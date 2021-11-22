# Tilnet Corteza Extension

Adjust the corteza-ext repo to Tilnet use-case

## Instruction for creating workflow

1. Create the workflow with the UI editor
2. Export the workflow to .json format
3. use  ./.workflowFromJson script or: In the terminal, transform the workflow to valid yml format

``
yq eval -P ~/Downloads/CRM-Quote-Pdf-SendToPriContact.json | sed -E 's/parentID:\s"([^"]+)"/parentID: \1/g' | sed -E 's/childID:\s"([^"]+)"/childID: \1/g' | sed -E 's/stepID:\s"([^"]+)"/id: \1/g'
``
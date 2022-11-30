## Installation

```shell
git clone https://github.com/yangxyo/document-editor-vue2.git
```

## Usage

Find below the component usage example:

```vue
<template>
  <DocumentEditor
    id="docEditor"
    documentServerUrl="http://documentserver/"
    :config="config"
    :events_onDocumentReady="onDocumentReady"
  />
</template>

<script lang="ts">
import { DocumentEditor } from "@/components/document-editor-vue2";

export default {
  name: "ExampleComponent",
  components: {
    DocumentEditor,
  },
  data() {
    return {
      config: {
        document: {
          fileType: "docx",
          key: "Khirz6zTPdfd7",
          title: "Example Document Title.docx",
          url: "https://example.com/url-to-example-document.docx",
        },
        documentType: "word",
        editorConfig: {
          callbackUrl: "https://example.com/url-to-callback.ashx",
        },
      },
    };
  },
  methods: {
    onDocumentReady() {
      console.log("Document is loaded");
    },
  },
};
</script>
```

## API

See：https://github.com/ONLYOFFICE/document-editor-vue#api

<template>
  <editor-content :editor="editor" />
</template>

<script>
  import { useEditor, EditorContent } from '@tiptap/vue-3';
  import StarterKit from '@tiptap/starter-kit';

  export default {
    components: {
      EditorContent,
    },

    setup() {
      const editor = useEditor({
        content: "<p>test test test",
        extensions: [
          StarterKit,
        ],
      })
      return { editor }
    }
    
  };
</script>

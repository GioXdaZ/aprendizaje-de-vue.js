<script>
import BlogPost from "./BlogPost.vue";

export default {
  components: {
    BlogPost,
  },
  data() {
    return {
      posts: {
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean quis quam lorem. Ut convallis enim malesuada nibh convallis, eget aliquam elit viverra. Curabitur eu sem interdum, pellentesque sapien a, tempus quam. Suspendisse ligula ante, pulvinar vel posuere ac, sollicitudin id nunc. Pellentesque vehicula felis elit, in iaculis diam tincidunt eget. Pellentesque pulvinar eros odio, ac gravida ligula pharetra eu. Integer semper est vitae ligula posuere ultricies. Etiam massa ante, lobortis quis suscipit vitae, porta vitae orci. Fusce varius leo eget erat volutpat pharetra. Etiam pharetra purus nisi, eu bibendum quam rutrum sit amet.",
      },
      postFontSize: 100,
    };
  },
  methods: {
    enlargeText() {
      this.postFontSize += 10;
    },

    reduceText() {
      this.postFontSize -= 10;
    },
  },
  computed: {
    styleText() {
      return {
        fontSize: this.postFontSize + "%",
      };
    },
  },
};
</script>

<template>
  <div class="container flex flex-col justify-center items-center gap-4">
    <h1>Re-Size Text</h1>
    <div>
      <BlogPost
        @enlarge-text="enlargeText"
        :fontSize="postFontSize"
        @reduce-text="reduceText"
      >
        <div :style="styleText">{{ posts.text }}</div>
      </BlogPost>
    </div>
  </div>
</template>

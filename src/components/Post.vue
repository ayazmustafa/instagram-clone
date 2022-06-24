<template>
  <div class="post">
    <!-- header -->
    <header class="header section">
      <div class="header-author">
        <Avatar :size="40" />
        <div class="header-author-info">
          <div>
            <CustomText tag="b">Mustafa Ayaz</CustomText>
          </div>
          <div>
            <CustomText size="xsmall">Istanbul, Turkey</CustomText>
          </div>
        </div>
      </div>
      <div class="header-more">
        <button type="button">
          <IconMore />
        </button>
      </div>
    </header>

    <!-- media -->
    <div class="post-media">
      <img
          src="https://media.discordapp.net/attachments/986699863938990082/989978347603918898/frog.png"
          alt=""
          width="100%"
      />
    </div>

    <!-- actions -->
    <div class="action-buttons section">
      <button type="button">
        <IconLike />
      </button>
      <button type="button">
        <IconComment />
      </button>
      <button type="button">
        <IconDirect />
      </button>
      <button class="action-save"
              type="button"
      >
        <IconSave />
      </button>
    </div>

    <!-- view count -->

    <div class="view-count section">
      <custom-text tag="b">1.122 beğenme</custom-text>
    </div>

    <!-- comment list -->

    <!-- datetime -->

    <!-- comment form -->
  </div>
</template>

<script>
import Avatar from '@/components/Avatar';
import CustomText from '@/components/CustomText';
import IconMore from '@/icons/more.svg';
import IconLike from '@/icons/like.svg';
import IconComment from '@/icons/comment.svg';
import IconDirect from '@/icons/direct.svg';
import IconSave from '@/icons/save.svg';

export default {
  name: 'Post',
  components: {
    IconLike,
    IconComment,
    IconDirect,
    IconSave,
    IconMore,
    CustomText,
    Avatar
  }
};
</script>

<style scoped>
.post {
  border-radius: 3px;
  border: 1px solid rgb(var(--b6a));
}

.section {
  padding-left: 16px;
  padding-right: 16px;
}

.header {
  height: 60px;
  display: flex;
  align-items: center;

  &-author {
    display: flex;
    align-items: center;

    &-info {
      margin-left: 8px;
    }
  }

  &-more {
    margin-left: auto;
  }
}

.action-buttons {
  height: 45px;
  display: flex;
  align-items: center;

  button {
    margin-right: 16px;
  }

  .action-save {
    margin-left: auto;
    margin-right: 0;
  }
}
</style>
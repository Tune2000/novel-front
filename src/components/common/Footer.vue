 <template>
  <div class="footer">
    <div class="box_center cf">
      <div class="copyright">
        <ul>
          
          <li>
            所有小说和章节均由网友上传，转载只为宣传本书让更多读者欣赏
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { useRouter } from "vue-router";
import { getToken } from "@/utils/auth";
export default {
  name: "Footer",
  setup() {
    const router = useRouter();
    const goFeedBack = () => {
      if(!getToken()){
        router.push({name: 'login'});
      }else{
      router.push({name: 'feadback'});
      }
    };
    return {
      goFeedBack
    }
  },
  
};
</script>
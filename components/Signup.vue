<template>
    <section class="signup-form [ container-narrow ] []">

        <div v-if="success">
            <div class="install-app-text">
                <p>Vi har modtaget din ansøgning om at komme med på Moooce-bølgen fra start.</p>
                <p><strong>Tusind tak, vi er glade for at du vil være med. </br> Vi vender tilbage ASAP!</strong></p>
            </div>
        </div>
        <form v-else name="Moooce tester" method="POST" action="/signup/success/" netlify>
            <label>
                <span>CVR nr. <sup>*</sup></span>
                <input type="text" id="cvr" name="cvr" required>
            </label>
            <label>
                <span>Virksomhed <sup>*</sup></span>
                <input type="text" id="company" name="company" required>
            </label>
            <label>
                <span>Land <sup>*</sup></span>
                <select id="country" name="country" >
                    <option value="" selected></option>
                    <option value="dk">Danmark</option>
                </select>
            </label>
            <label>
                <span>Email (Til kontakt) <sup>*</sup></span>
                <input type="email" id="email" name="email" required>
            </label>
            <label>
                <span>Din E-COMMERCE URL <sup>*</sup></span>
                <input type="url" id="url" name="url" value="https://" required>
            </label>
            <div class="signup-form__start cluster bg-primary p-200 space-300">
                <Checkbox text="Ja, I må gerne sende mig emails." />
                <button name="subscribe" id="mc-embedded-subscribe" class="btn" data-type="secondary">Start nu</button>
            </div>
            <input type="hidden" name="form-name" value="Moooce tester" />
        </form>
        <div v-if="success" class="col-lg-8 offset-lg-2 col-md-8 offset-md-1">
            <div class='embed-container'><iframe src='https://www.youtube.com/embed/IpyPb339r_M?modestbranding=1&playsinline=1&iv_load_policy=3' frameborder="0" allowfullscreen></iframe></div>
        </div>
    </section>
</template>

<script>
import Checkbox from '@/components/Checkbox'

export default {
    name: "TesterForm",
    components: {Checkbox},
    props:{
        success: {
            type: Boolean,
            default: false
        }
    }
};
</script>

<style lang="scss" scoped>

.signup-form{
    &__start{
        border-radius: 10rem;
    }
}

</style>
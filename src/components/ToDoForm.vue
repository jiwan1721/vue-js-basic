<template>
    <form @submit.prevent="onSubmit"> <!-- yesley page reload huna didaiina -->
        <label for="new-todo-input">
            what needs to be done?
        </label>
        <input
            type="text"
            id="new-todo-input"
            name="new-todo"
            autocomplete="off"
            v-model.lazy.trim="label"
            class="input__lg"
        />
        <button type="submit" class="btn btn__primary btn__lg">Add</button>
    </form>
</template>
<script>
    export default{
        methods: {
            onSubmit(){
                console.log('label value: ',this.label);
                if(this.label=== ""){
                    return;
                }
                this.$emit("todo-added",this.label);
                this.label="";
            }
        },
        //we need a way to get the value from the forms input
        data() {
            return {
                label: ""
            };
        }
    };
</script>
<template>
    <div class='container'>
        <div class='card rounded mb-3 p-3'>

            <label>Title</label>
            <input type='text'/>

            <label>Publish Date</label>
            <input type='date'/>

            <label>Featured?</label>
            <input type='checkbox'/>

            <label>Collaboration?</label>
            <input type='checkbox'/>

            <label>Image</label>
            <input type='file'/>

            <label>Language</label>
            <input type='text'/>

            <label>Description</label>
            <textarea/>

            <label>Deployed Link</label>
            <input type='text'/>

            <label>GitHub Link</label>
            <input type='text'/>

            <label>Support Status</label>
            <select>
                <option default disabled>Select support status</option>
                <option value='active'>Active</option>
                <option value='inactive'>Inactive</option>
                <option value='discontinued'>Discontinued</option>
            </select>

            <label>Application Type</label>
            <select>
                <option default disabled>Select application type</option>
                <option value='client-side'>Client Side</option>
                <option value='server-side'>Server Side</option>
                <option value='unified'>Unified</option>
            </select>

            <label>Keywords</label>
            <input type='text'/>

            <br/><br/>

            <div class='btn btn-primary'>Submit</div>
            
        </div>
    </div>
</template>

<script>

export default {
    name: 'AppCard',
    props: []
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>

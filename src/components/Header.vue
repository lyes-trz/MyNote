<template>
    <div class="row">
        <div class="logo">
            <img src="src/assets/mynote-logo.png" style="width:80px; height:auto;" >
            
        </div>
        <div class="col-sm-12">
            
            <div class="progress" style="width: 50%;  position: absolute;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  margin-top: 50px;">
                <div class="progress" >
                    <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="background-color: #ff6464;" 
                        :style="{width: (noteCount / maxNotes) * 100 + '%'}">{{ noteCount }} / {{ maxNotes}}</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['noteCount', 'maxNotes']
    }
</script>

<style>
    .logo{
        text-align:  center;
        margin-top: 40px;
        margin-bottom: -10px;
    }
</style>
<template>
    <div class="container">
        <table class="table table-hover">
            <thead class="thead-light">
            <tr>
                <th scope="col">#</th>
                <th scope="col">Title</th>
                <th scope="col">Content</th>
                <th scope="col">Person In Charge</th>
                <th scope="col">Show</th>
                <th scope="col">Edit</th>
                <th scope="col">Delete</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="i in 3" :key="i">
                <th scope="row">{{i}}</th>
                <td>Title1</td>
                <td>Content{{i}}</td>
                <td>Ichiro</td>
                <td>
                    <router-link v-bind:to="{name: 'task.show', params: {taskId: 1}}">
                        <button class="btn btn-primary">Show</button>
                    </router-link>
                </td>
                <td>
                    <router-link v-bind:to="{name: 'task.edit', params: {taskId: 2}}">
                        <button class="btn btn-success">Edit</button>
                    </router-link>
                </td>
                <td>
                    <button class="btn btn-danger">Delete</button>
                </td>
            </tr>

            </tbody>
        </table>
    </div>
</template>

<script>
    export default {}
</script>
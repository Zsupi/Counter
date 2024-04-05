<script lang="ts">
    import { Confetti } from "svelte-confetti"
</script>

<div class="fixed top-[-50px] left-0 h-screen w-screen flex justify-center overflow-hidden pointer-events-none">
    <Confetti x={[-5, 5]} y={[0, 0.1]} delay={[500, 2000]} infinite duration={5000} amount={200} fallDistance="100vh" />
</div>

<div class="flex min-h-screen justify-center items-center">
    <h1 class="h1">Thanks 😊</h1>
</div>
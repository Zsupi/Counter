<script lang="ts">
    import { Avatar } from "@skeletonlabs/skeleton";
    import SocialIcons from '@rodneylab/svelte-social-icons';
    import avatar from "../assets/avatar.png";

    const requestDate = new Date('2024/04/05');
    const today = new Date();

    const done = false

    function calculateDaysBetween(date1: Date, date2: Date) {
        const oneDay = 1000 * 60 * 60 * 24;
        const diffInTime = Math.abs(date2.getTime() - date1.getTime());
        return Math.ceil(diffInTime / oneDay);
    }
</script>

<div class="container min-h-screen mx-auto flex justify-center items-center">
    <div class="space-y-10">
        <h1 class="h1">Can you draw my Profile 🥺👉👈</h1>
        <div class="flex justify-center items-center">
            <Avatar src={avatar} width="w-40" rounded="rounded-full"/>
        </div>
        <a class="block card p-4 text-center text-2xl" href="/">Day {calculateDaysBetween(today, requestDate)} of asking to draw me</a>
        <div class="flex justify-center items-center">
            <a href="https://www.instagram.com/nemeth1375/">
                <SocialIcons network="instagram" fgColor="#eeeeee" bgColor="#2e395a"/>
            </a> 
        </div>
    </div>
</div>
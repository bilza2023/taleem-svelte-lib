<script>
    import {Anchor,AnchorIconOval,PageWrapper,AreYouSure,HdgWithIcon} from "../lib"
</script>

<PageWrapper backgroundColor="#094206">
  <div class='flex flex-col gap-2'>

<Anchor href="/about" id="link-about" aria-label="About Us">About</Anchor>

<HdgWithIcon
  icon="🔥"
  headingText="Hot Topic"
  fontSize="2rem"
  backgroundColor="#f9f9f9"
  textColor="#ff5733"
  textAlign="center"
/>

<AreYouSure warningText='sure.?' />

<AnchorIconOval
  href="/settings"
  iconName="BULB"
  style="
    --anchor-icon-oval-bg: #e74c3c;
    --anchor-icon-oval-hover-bg: #c0392b;
    --anchor-icon-oval-color: #fff;
  "
>
  Settings
</AnchorIconOval>


</div>
</PageWrapper>

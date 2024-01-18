<FirstPage/>

<TOC/>

[[toc]]

<TransitionGroup>

<div class="h" :class="{'appear': counter >= 1}" data-scroll-id="1" :key="1">

## Reshaping Global Investment I {#h-1}

The world is changing, much that was once known is being rewritten, the investment landscape of the future
will look very different from the one taught in text books and used as references for risk metrics and advisory.
The political dynamics are shifting globally and new financial power-house centers are emerging, reshaping
the world from a Western-centric economic system, primarily driven by American interest, to a Multi-polar
landscape driven by a diverse set of political interests that sometimes align, and sometimes clash. In such
a landscape, the task of the average investor is somewhat complicated by the lack of simple guidelines on
how to allocate wisely. Simple rules such as the 40:60 which have dominated over the previous century no
long provide the growth necessary to justify the passive investment, “flight to safety” no longer provides
the protection it once could, even the sanctity of the free market has been undermined since the very first
round of quantitative easing.

Successfully navigating this brave new world requires a slightly different toolset, a marginal shift in mindset,
and an adjustment in how opportunities are assessed and risk is measured. This 12-part series “Reshaping
Global Investment” provides investors with the tools to assess and surf this changing world environment and
position themselves as truly global investors. The series is divided into four main topics with three articles
each.

The first topic “Health of Nations” deals with methods to measure and compare alternative investment
regions, to assess where capital is flowing, where value is being created, and which nations or regions
are supporting policies and regulatory regimes conducive to successful investing. The structure provides
investors with the means to construct measurable statements, not only that a country is good, but rather
to assess if, relatively speaking, it is better than others, and thereby derive the rationale behind why certain
regions deserve more investor focus.

The second topic “Adventurous Capital” provides a strategy for sketching an investment vision, formalizing it
into a structural strategic framework, and rationalize investment decisions to tackle potential growth regions
that are traditionally outside of the scope of safe-haven funds and market tracking ETFs. This segment draws
on historical time periods where broad political shifts have occurred, much as is happening now, and how
to face the challenges and opportunities and strategically position investment portfolios to ride the gains
and cushion the drawdowns.

The third topic “Evaluating Assets” deals specifically with asset class performance under alternative market
conditions. When traditional safe havens no longer offer sanctuary from market volatility a strategy is
required to determine how to optimize the tactical allocation and mitigate portfolio risk to weather the
storm and not just survive, but thrive.

The final topic “Resilient Portfolios” expounds on the whole process for independent investors, fund
managers, and CIOs to implement into their existing structures to provide an additional layer of security to
decision making. The process ties together the regulatory, reporting, and client-facing communications
and illustrates how naturally they fit within the investment framework.

</div>

</TransitionGroup>

<TransitionGroup>

<div class="h" :class="{'appear': counter >= 2}" data-scroll-id="2" :key="1">

### Health of Nations {#h-2}

The first installment of the investment series Reshaping Global Investment uses the Health of Nations
Indicator (1) to see how major movements over the last two decades have restructured global investment
opportunities.

The first article assess long-term trends in the general macro, financial, and political environment and the
implications on the relative health of the United States versus their emergent Asian counterpart China.

The second article compares the two major Asian territories, India and China, and why one has emerged as
an investment power house while the other has lagged behind. The third story looks at Indonesia compared
to the Philippines to show how local players can provide intriguing investment opportunities.

</div>

</TransitionGroup>

<script setup>
import { ref, onMounted, nextTick } from 'vue'
let counter = ref(0),
  headings = ref([])

onMounted(() => {
  console.log(1);
  setTimeout(() => {
    headings.value = Array.from(document.querySelectorAll(".h")).map(el => {
      return {
        id: el.getAttribute("data-scroll-id"),
        top: el.offsetTop
      }
    });
    console.log(headings.value)
  }, 500)
})

document.addEventListener("scroll", (e) => {
  console.log(window.scrollY, (3 * window.innerHeight / 4), headings.value[0].top);
  if(window.scrollY + (3 * window.innerHeight / 4) >= headings.value[0].top) {
    let el = document.querySelector(`.h[data-scroll-id="${headings.value[0].id}"]`)
    console.log(el);
    el.classList.add("appear");
    headings.value.shift();
  }
})
</script>
# From Chaos Engineering to Parenting: When My Kids Inject the Failures for Me

## This morning, 10:23 AM, grooming area

Everything was perfectly orchestrated. After a catastrophic morning at home, I'd gathered my courage and taken my two boys to see Vazy, my mare. Journey: everyone falls asleep. Arrival: the stable manager is there to watch the sleepers while I fetch my mare from the field. My toddler wakes up at exactly the right time. We go get the grooming equipment together. The baby wakes up gently. I put him on the ground, away from the hooves. Everyone plays quietly.

And then.

Victor the golden retriever, adorable clumsy puppy of the manager, arrives at full speed to say hello.

He tries to play with the brush my toddler is holding. The brush flies into stagnant water. My son loses his balance, falls. The golden, enthusiastic, continues his momentum to lick my baby, knocks him backwards. Then climbs into the borrowed car—covered in mud—to check if there might be a third child to play with.

Everyone's crying. My mare is on edge. Victor is very proud of himself.

Me? I don't know whether to laugh or tear my hair out.

At ManoMano, I voluntarily injected failures into systems to test their resilience. Now I don't need to inject anything. My kids handle it.

---

## Chaos Engineering 101: When Breaking Things Becomes a Skill

Chaos Engineering is the art of voluntarily introducing failures into a system to verify it can handle them. At ManoMano, I would cut production servers, simulate network latencies, provoke database crashes. Not out of sadism. To ensure that when the real catastrophe arrives, the system holds up.

The objective: identify weak points before they become critical incidents in the middle of the night.

A family with two young children is exactly the same thing. Except that:
- The failures aren't simulated, they're constant
- The system runs 24/7 with no possibility of planned maintenance
- The components (the children) constantly evolve, changing test conditions
- And ESPECIALLY nobody gave you the user manual

Welcome to my involuntary Chaos Engineering laboratory.

---

## My Personal Chaos Monkeys: When Kids Do Family Fuzzing

You know the nursery rhyme? *"3 little monkeys jumping on the bed, one fell off and bumped his head..."* In Chaos Engineering, we have Chaos Monkeys too. Tools invented by Netflix that voluntarily kill production servers to force teams to build resilient systems.

At my house, I have two Chaos Monkeys. Except they don't kill servers, they spill tea, corrupt clean laundry, and hack the intercom. And unlike the rhyme, they never fall off the bed. For them, it's everything else that falls.

**Scenario 1: Well-Intentioned Help**

My toddler loves to "help" fold laundry. Touching, right? Except he takes the last t-shirt from the clean, carefully folded pile, unfolds it, and puts it in the closet. Or better: he empties the clean washing machine directly into the dirty laundry bin.

It's pure error injection. The "clean laundry → closet" system gets corrupted. And the worst part? It comes from good intentions. Like a junior developer deploying an untested fix to prod.

**Scenario 2: The Tea Spill**

I'm changing my baby. I hear the sound of a metal box falling in the kitchen. I ask my toddler what he's doing. The activity is too fascinating for him to answer. When I come out of the bathroom with baby in my arms, I discover he wanted to smell all my teas. Result: sachets everywhere on the floor, mixed fragrances, total chaos.

Unintentional data corruption. The "tea sorted by type" system became "tea scattered on the tile". And I have to clean while the baby starts crawling toward the disaster.

**Scenario 3: The Budding Hacker**

My toddler has an innate talent with electronics. He presses all the intercom buttons and manages to set it to silent mode. Result: when the diaper delivery person arrives, we don't hear them. They leave without dropping off the package. And of course, it's the day the diapers run out.

It's interface fuzzing. He tests all possible button combinations until he finds one that changes the system's behavior. Except unlike the "rosebud" cheat code from The Sims I used as a kid to get infinite money, here, there's no rollback possible.

---

## Family Blast Radius: When a Failure Propagates in Cascade

The golden retriever cascade is a textbook case of uncontrolled blast radius.

**Initial incident**: Enthusiastic dog arrives too fast.

**Propagation level 1**: Brush flies → child falls → stress rises.

**Propagation level 2**: Dog continues → second child falls → generalized crying.

**Propagation level 3**: Dog climbs into forbidden car → mud everywhere → stressed mare.

**Final impact**: Family system in degraded mode. All components affected simultaneously. Recovery time: 15 minutes of hugs + car cleaning.

It's exactly what happens when a microservice fails and all downstream dependencies start failing. Except here, I don't have a Grafana dashboard to monitor crying-per-minute metrics.

Another example: the intercom in silent mode.

**Initial incident**: Accidental setting by curious toddler.

**Propagation level 1**: Delivery person can't notify → no delivery.

**Propagation level 2**: Diaper stock reaches zero.

**Propagation level 3**: Impossible to go out and buy diapers (two kids + no diapers = impossible equation).

**Final impact**: Emergency escalation. Call husband. Detour to pharmacy on way home from work.

The blast radius of a simple intercom button: the entire family organization.

---

## Predictable Failure Scenarios: Failures You See Coming (But Can't Always Prevent)

Some failures, we know them. We see them coming. But sometimes, we simply don't have the resources to prevent them.

**The Overloaded Diaper**

Every morning, I wake up tired. My toddler has enormous diapers. I know that if I don't change him immediately, it will overflow. But sometimes he categorically refuses. He runs everywhere. And I must choose: fight now and risk a generalized nervous breakdown, or accept the overflow risk.

It's like knowing a server is at 95% RAM and will crash in 10 minutes, but restarting now would cut service to connected users. You temporize. You hope. And sometimes it holds. Sometimes not.

**The Optimized Morning Routine**

To avoid morning failure scenarios, I've implemented a routine: wake the baby first, change him, install him with a piece of bread. While he's occupied, I go get my toddler. I leave him without pants (graceful degradation: if the diaper overflows, no need to change pants).

It works. Except when the baby doesn't want bread anymore. Or when the toddler refuses to be changed. Or when both wake up at the same time. Predictable failure scenarios aren't always avoidable. They're just... predictable.

---

## Parental Circuit Breakers: Knowing When to Cut the System

A circuit breaker is a mechanism that automatically cuts the flow when the system is overloaded. It prevents complete degradation.

In family, it's the same. There are moments when you must activate the circuit breaker manually.

**The other morning, everyone was upset.** The baby was whining for no reason. The toddler was overexcited and listening to nothing. The dog was barking. My husband was with his headphones in front of the computer while an atomic bomb was exploding in the next room.

I thought about calling my mother for backup. Not available.

So I activated the family circuit breaker: I strapped everyone into the stroller, went down to the car, and decided to go see Vazy. Radical context change. New system, new conditions. And it worked. Everyone fell asleep within 5 minutes.

The circuit breaker is knowing how to say: "This system is spiraling out of control. We cut. We change environments. We restart."

Sometimes it's a call to a friend: "Are you free for a walk in the park?" Sometimes it's ordering pizza instead of cooking. Sometimes it's just sitting on the balcony with the crying baby and waiting for energy to return.

The parental circuit breaker isn't abandonment. It's critical incident prevention.

---

## Resilience Patterns: The Strategies That Keep the System Running

Some resilience patterns become automatic.

**Occupational bread**: Install the baby with a piece of bread while I handle the toddler. It's like a cache: it occupies the CPU (the child) while I process other requests.

**No-pants mode**: Leave the toddler in a diaper in the morning to avoid having to change pants in case of overflow. It's graceful degradation: we accept a degraded mode (not dressed) to avoid complete failure (dirty pants + battle to put on clean ones).

**Double stock**: Always have a spare bag in the stroller. Always have backup diapers in the car. It's redundancy. If one component fails, the backup takes over.

These patterns aren't glamorous. But they're what keeps the family system running even when everything goes haywire.

---

## Blameless Post-Mortem: Learning from What Went Wrong

Visits to the grandparents are our recurring post-mortem.

We systematically debrief after each visit. Not to find someone to blame. To understand what went wrong and how to avoid it next time.

**Lesson 1**: Even if we ask for lunch around noon, nothing is ever ready before 1:30 PM. Solution: bring baby food + milk to feed the kids at the first signs of hunger.

**Lesson 2**: Delaying lunch delays the nap. Solution: slip away before the end of the meal if necessary. Children's needs > politeness.

**Lesson 3**: If there's underlying tension at the grandparents', our children (emotional sponges) pick up everything and derail. Solution: leave at the first opportunity. Children's well-being first.

It's a post-mortem that isn't perfect yet. We iterate. We adjust. But we don't blame each other. We learn.

Like after a production incident: we identify the root cause, we implement preventions, we improve monitoring. No blame, just learnings.

---

## Parental Antifragility: Getting Stronger Through Chaos

Antifragility is when a system doesn't just resist stress, but becomes stronger because of it.

My toddler tries to crack the front door code. He presses all the buttons. Result: he rings the neighbors' doorbell. And it turns into an impromptu happy hour.

A failure that becomes a feature. An incident that creates social connection.

Or again: the golden retriever cascade. In the moment, it was total chaos. But after? We laughed. We cleaned together. My toddler learned to be more careful with excited dogs. And I understood that even my "refuge" outings could go haywire, and that was okay.

Each family micro-catastrophe makes me a bit more resilient. A bit more capable of handling the unexpected. A bit more antifragile.

Because chaos doesn't weaken the system. It strengthens it. As long as you don't passively endure it, but learn from it.

---

## What This Teaches Me as a Product Owner

At ManoMano, I injected chaos to test system resilience. Now I live in chaos to learn how to build resilient systems.

A good product isn't a product that never fails. It's a product that knows how to absorb failures and continue functioning.

As a future Product Owner, I will know how to:
- Identify breaking points before they become critical
- Implement circuit breakers to avoid complete degradations
- Design resilience patterns that maintain service even in degraded mode
- Conduct constructive post-mortems without looking for culprits
- Build antifragile systems that improve under pressure

Because every day, I manage a complex distributed system with unpredictable components, constant failures, and zero possibility of rollback.

And if I can manage that, I can manage any product.

---

**What about you—what's your worst family incident cascade?**

Share your blast radius in the comments. Because the best resilience lessons always come from the field.

---

## About me

I'm Cecilia, former Chaos Engineer at ManoMano, former Cloud Engineer at Ubisoft, former saddle-fitting entrepreneur, and future Product Owner. From voluntary Chaos Engineering to involuntary parental chaos, I've learned that resilience is built through adversity.

**I will be available for new Product Owner opportunities starting November/December 2025.**

If you want to see how I translate these skills into concrete product methodology, **[my portfolio is here](https://tar-hawk-fa8.notion.site/Portfolio-Product-Owner-Cecilia-DI-MAULO-27bd1b694d528029a1e9c2258667a3bf)**.

My tea is cold, but my systems are resilient. ☕💪
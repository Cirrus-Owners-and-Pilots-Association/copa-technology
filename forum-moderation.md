# COPA Forum Moderation: The Automated Civility Check

> **Status: DRAFT** — describes the system as it is being rolled out in October 2026. Last updated 3 October 2026.

COPA's forums are moderated by volunteer members. Since August 2026 they have had help from an automated check that reads new posts and flags personal attacks. This document explains what the check does, what it does not do, what happens when it acts on a post, and how members can get a post restored. It is published here so the rules are visible to everyone they apply to.

## 1. What it checks

The check looks at one thing: whether a post attacks a person rather than an argument. COPA's guidelines and the OMUP Best Practices already ask members to argue with what people say, not who they are. The check applies that rule.

It flags a post when the author's own words do any of the following to a member, a group of members, or an identifiable person:

- use a slur;
- make a sexual or crude remark about someone;
- call someone a demeaning name, or aim profanity at them;
- label someone as brainwashed, deranged, stupid, a victim, or similar, including dressed up as a diagnosis;
- direct contempt or ridicule at who someone is rather than at what they said;
- talk down to someone about their intelligence, literacy or sincerity;
- belittle someone for their age, appearance or sex;
- make a serious criminal or sexual accusation against anyone, including a public figure;
- keep taking shots at the other person in an exchange that has already turned hostile.

It judges the target, not the vocabulary. "That claim is nonsense" is criticism of a claim. "You're too thick to understand it" is not.

## 2. What it does not do

- **It does not judge political content.** Heated political argument, criticism of governments, companies and public figures, and unpopular opinions all pass. Political posts are handled by the human moderators under the existing guidelines, the same as before.
- **It does not read quotes against you.** Text you quote from someone else is not held against you. Quoting an insult in order to object to it passes.
- **It does not punish banter.** Friendly ribbing between members who are evidently on good terms passes, even when the words would read as rude out of context.
- **It does not delete posts, silence anyone, or suspend anyone.** The only thing it can do is hide a post and put it in front of a moderator.
- **It does not look at staff posts**, and it does not run in the marketplace categories or Guest Discussion.

## 3. What happens when it flags a post

1. The post is hidden within a few seconds of being published. Other members do not see it.
2. The author receives a message saying the post was hidden by the automated civility check, with a link to the post and a one-sentence reason.
3. The post goes into the moderators' review queue with the check's reason attached.
4. A moderator reads it and decides. If the moderator disagrees with the check, the post is restored and nothing else happens. If the moderator agrees, the post stays hidden or is removed under the normal guidelines.

The author can also edit the hidden post after ten minutes, and it reappears automatically. If the edited post is flagged again, it stays hidden until a moderator looks at it.

**A human makes every final decision.** The check's hide is a hold, not a verdict.

## 4. How it reads a post

For each new post in a covered category, the check reads the topic title, the preceding posts in the thread, and the new post, and decides against the rules in Section 1. It writes a one-sentence reason, a category (which rule), and a severity. Only the reason and category are shown to the author and the moderators. The reading is done by a large language model (Claude, by Anthropic) under COPA's own account. Post text sent to the model is not used to train it under the API terms COPA operates under. Nothing is sent that is not already visible on the forum.

The covered categories are Off Topic, General Aviation, Cirrus Flying, Airframe & Powerplant Issues, Avionics, Accident Reports and COPA Organization, including their subcategories. This list can change; the current list is always in this document.

## 5. How well it works

Before switching on automatic hiding, the check was tested against two years of real moderation decisions on these forums: 568 posts that moderators had removed or that members had flagged, judged with the surrounding thread included.

- Of the posts moderators had removed for personal attacks, the check caught about three in four.
- When the check flagged a post, a moderator had agreed it was a problem about four times in five.
- If every one of its flags had been an automatic hide, moderators would have reversed about one in five. At current forum traffic that is roughly two hides a day and a couple of reversals a week.
- Half of what moderators remove is political content, which the check deliberately does not touch.

It is not perfect and will not be. It misses some sarcasm, and it will occasionally hide a post a moderator then restores. The moderators' reversals are the main signal used to tune it.

## 6. Reporting and changes

- The number of posts hidden, the number restored by moderators, and the reversal rate are reported to the board monthly and summarized to members in the build forum category.
- The rules in Section 1 are the plain-language version of the instructions given to the model. Changes to those instructions are recorded in this repository's changelog with the date and the reason.
- The check runs on COPA's own accounts and can be switched off by the Director of Operations or the technology lead at any time. If it is switched off, moderation continues by hand as before.

## 7. If you think the check got it wrong

Say so. If your post was hidden and a moderator restored it, nothing further is needed; that is the system working. If it was hidden and kept hidden and you disagree, reply to the hidden-post message or contact the moderators the usual way. Patterns of wrong flags are the most useful feedback there is, and they change the rules.

## 8. Who maintains this

The technology lead maintains the check and this document, with the moderator team. Changes to what the check looks for (Section 1) are agreed with the moderators and reported to the board. Switching the check from hiding posts back to review-only, or extending it to new kinds of content such as political posts, is a board decision.

## Write better commit messages!

# Commit messages are mostly useless

Commit messages are really not that useful! you can argue as much as you want only if people did it this way or only if they implemented that set of standards. 

*Commit messages will still be useless!*

## Why?

All teams use some sort of git host like GitHub. and all of these services provide much better tooling to have a discussion around the feature you added or the bug you just fixed. Why would you use the commit body to explain what you did? what is the point? While you have a really nice UI with a nice text editor and you can tag your teammates and they can respond to you?

**With this mindset let's think about what do we need in our commit messages.
**

## State your intent & Make it shorter

I hate long commit messages no one is going to read a long commit message.
So declare your intent is it a fix, feature, enhancement, or a refactor.

The enhancement flag is for developer-related features. added linting, CI/CD enhancement, introduced a tool, docs, add tests, etc.

Write in 10 words or less what you made. e.g 
- fix/login-screen-validation
- refactor/class-a-to-introduce-endpoint-b

## Reference the issue
As I said at the beginning commit messages are redundant because we don't need them to add context or start a conversation.
So we need to bring context to our changes. The best context you can provide is where did this start so reference the issue at the commit. and have your conversation on the issue. this makes it accessible for devs, PM and QCs

You can use ref #<Issue-ID> which refers to the commit and add a comment to the original issue. this is supported by almost all of the Git hosting services.

I dislike close, fix and I prefer to do this manually from the issue itself as usually need to add final remarks but you can sometimes use them for hotfixes or something.

## Details are for PRs

What the told you to add in the commit message you can write it here. it's much clearer and more visible this way! here you should

1. What have you changed in detail?
2. Why have you made these changes?
3. Keep it short & use bullet points.
4. Emojis are fun please use them more.

## Stylistic preferences

You can write however you like but if you are not so great at writing like me I find these guidelines nice to follow.

1. Start with a verb I find past tense makes more sense.
Rename class A to B. VS Renamed class A to B!
2. Stick to bullet points
3. Add a conclusion sentence "If applied, this commit will achieve X"








 
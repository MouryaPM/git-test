git --version : to check versions 
git status : to get status of git
git init   - initialize git repo 
git add . -> track our files

git commit.txt -> to add single files


git log 

git branch branchname 

git branch 

git checkout branchname



git check out -b branchname



connect local to github repor 
git remote add origin url 
this will establish a connection 


command : git push origin main 

origin - github repo 
main -> master in our case

when we enter this command it will ask for email and password 


we need a personal access token to push the data to our github repo 

click on signed in as -> settings -> developer settings -> personal acccess token 

name , expiration 
select eveything othe rthen admin  part 

click ok -> token generated

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 -> token 

show output in github , 

NExt step lets add next file here
git add .
git commit -m '' .
git push 

we see only one file then where are our rest of the files 

well click on commit and we get all the previous commit


try doing git branch now - this will give the branches we have

try doing now git branch -a 
we get one red branch as well 

Do we have more branches now?
Well, the answer is yes
and let's explore why this is the case?

With GIT remote at origin, we established
a connection between our local repository
and the remote repository so both repositories
are now able to connect so to say.

The thing is that this is not related to our branches
until we really pushed something to this remote repository.
And this pushing process is a bit more complicated
or maybe we should say it involves some more steps
than it may have seen.

Let's have a look at this approach we did, again
from a theoretical perspective.

We have our local branch and our machine,
this master branch we created.

We then run GIT at remote origin,
you know how this works, so as I said,

we have a connection to the repository available
and then we run this command here, GIT push origin master.

So we said GIT should push our local changes
from this branch to the origin,

so basically to our remote location off the repository
and specifically to the master branch,

we didn't have this master branch so it was created then
but this is what this command told us.

Now what then happened behind the scenes is
well GIT first created a so-called remote tracking branch,

that's this red branch you could see
when we added git branch-a in VS Code in a terminal.

Now this remote tracking branch is basically
between our local branch and the remote branch

so it's kind of a local copy of the remote branch
as we don't have a remote branch yet,

it's at the moment, a copy of our local master branch
because what's happening here now is that our changes

from the local master branch are copied so to say
into this remote tracking branch
and the remote tracking branch know where this

should go to because of origin master,
you can see this in both cases,

so we first have our master branch and here we have
the remotes origin master branch,

so remotes stands for, that's a remote branch in the end
and origin and master, all the know,
origin master, well, our repo and our branch.

And as soon as the remote tracking branch was created,
well, we also add these changes to our master branch
and that's now the remote branch in our origin repository.

So this is the flow.
So if you run GIT push origin master,
that's what's happening.

It's very important to understand
that there is no direct connection between our local branch

and the remote branch, so any kind of push

or pull operations always involve a remote tracking branch.

And as I said, the remote tracking branch is a local copy
of the remote branch but the remote tracking branch
is nothing we change here, we work in our local branch
in this case but it's basically
part of the updating process.

So it goes from master branch to remote tracking branch
and then to updating the remote branch.

This is not under the case for pushing branches.
We can, of course also retrieve data from our remote branch.

This works with GIT pull right here in origin master
and if you run such a pull command from our local branch,
well, then we first update our remote tracking branch again

because we tell GIT to update our origin master branch
again, right here and right there.

This means internally, GIT understands that we should update

this remote tracking branch with the GIT fetch command,

GIT pull is just a combination of GIT fetch

and GIT merge.

So we first say fetch the latest changes
from our remote master branch and add these changes
to the remote tracking branch,

and then that's the second step of GIT pull,
merge these changes into our local master branch.

It's very important to understand this flow right here
and I said that already to understand

that there is no direct connection
between the local branch and the remote branch.

The local branch is locally on our machine,
the remote branch is the branch on GitHub

and the remote tracking branch is a local read-only copy
of the remote branch so with that,

we always update the remote tracking branch first,
no matter if you push information or if you pull information

and then update the local branch or the remote branch.

that's the theoretical concept we have right here.

Now let's go back to our project




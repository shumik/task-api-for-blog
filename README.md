Create an API for blog application using Symfony and ApiPlatform covered with tests. You can
use Behat, PhpUnit or PhpSpec.
Anyone can register to the application and see all blog posts, but only verified users can add
and edit their blog posts. Blog post needs to have date, title and content. User needs to have
email, first name and last name.
User that wants to create their own blog post needs to send Verification Request to admin.
Verification Request flow:
1. User initiates Verification Request by sending image of their ID and an optional
message.
2. Verification Request is flagged with status ‘Verification requested’.
3. User can edit Verification Request until admin approves or declines it.
4. Admin can see list of all Verification Requests and filter them by user and status. Admin
can order them by date created.
5. Admin can approve Verification Request and user will be granted access for adding new
blog post. Verification Request is flagged with status ‘Approved’. User gets ‘Blogger’
role.
6. Admin can decline Verification Request and add the reason for rejection. Verification
Request is flagged with status ‘Declined’
7. User will get an email notifying them if their request was approved or declined

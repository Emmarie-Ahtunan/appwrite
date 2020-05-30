require 'appwrite'

client = Appwrite::Client.new()

client
    .set_endpoint('https://[HOSTNAME_OR_IP]/v1') # Your API Endpoint
    .setproject('5df5acd0d48c2') # Your project ID
    .setkey('919c2d18fb5d4...a2ae413da83346ad2') # Your secret API key
;

users = Appwrite::Users.new(client);

response = users.delete_session(user_id: '[USER_ID]', session_id: '[SESSION_ID]');

puts response
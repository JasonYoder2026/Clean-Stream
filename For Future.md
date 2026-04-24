# For future teams

## Known Issues
### Stripe
Currently, the Stripe keys are linked to a personal account of a dev for testing. A Stripe account for Clean Stream needs to be  
set up and the keys swapped. The public key is in the mobile client .env file and the private key is in the Supabase repository  
key store. (Supabase project dashboard -> Edge Functions -> Secrets) Replace STRIPE_SECRET_KEY with Clean Stream's. If the web app from Flutter project is still going to be used for payments, 
you need to create a webhook on Stripe using the stripeWebhook invocation URL and replace STRIPE_WEBHOOK_SECRET in Supabase with the new webhook secret. 

### Machine Communication
Without Nayax, machine communcation is mocked. The machine communication in the mobile repository calls edge functions pind-device and wakeDevice. 
These two functions should be able to be deleted and replaced with the real implementation when a service is decided upon and purchased. 


## Improvements

### Real-time on daily income widget
The dashboard widget displaying real time updates for dailying income subscribes to a channel in Supabase. Jake mentioned wanting to change it in the future. It is located in
the admin portal in src/supabase/repositories/TransactionRepository.ts in the subscribeToTodayRevenue function. 

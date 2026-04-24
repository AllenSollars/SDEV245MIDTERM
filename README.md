# SDEV245MIDTERM
The CIA Triad and entropy are things to consider when we talk about security.

Let us look at Confidentiality first.

We use something called AES-256 in GCM mode to keep things secret.

The information we want to keep secret is encrypted with a key that only the right person can get.

This person needs to know the passphrase to get this key.

Without the key it is very hard to turn the encrypted information into its original form.

AES-256 is a standard that has been approved by NIST. It is very safe.

There are many possible keys that it is not possible to try them all.

The GCM mode also helps us make sure that the information has not been changed.

If someone tries to change the encrypted information we will know because the decryption will fail.

Now let us look at Integrity.

We use something called SHA-256 hashing to make sure the information is correct.

Before we encrypt the information we make a code from it.

We store this code separately. Then we encrypt the information.

When we decrypt the information we make the code again.

If the two codes are the same we know that the information is correct and has not been changed.

SHA-256 is a one-way function, which means it is very hard to find two pieces of information that will make the same code.

It is also not possible to get the information from the code.

Finally let us look at Availability.

The symmetric encryption model helps us with this.

Because we use the key to encrypt and decrypt the people who are allowed to see the information can get it quickly and easily.

They do not need to depend on someone or a special server to get the information.

We store some information with the encrypted information, like the salt and the PBKDF2 iteration count.

This means that anyone who knows the passphrase can get the key and decrypt the information.

So the system is self-contained and works well.

 # lambda_pg_activerecord_layer


This is an lambda layer for making activerecord and pg work with aws lamda. when deploying to lambda compiling for that enviornment is a real pain.

i am making this as a repo hopping it can redude your suffering atleast a little bit.



Thanks to @mphsi for the initail code that i used to build upon

https://github.com/mphsi/ruby_lambda_pg_layer

# the section under is copy pasted and transalted from https://github.com/mphsi/ruby_lambda_pg_layer 's readme


Lambda layer designed to include the 'pg' gem in lambda-ruby functions.

Under the / ruby directory are all files generated after running 'bundle install --path =.'.
Under the / lib directory are the dependencies for the gem. These files I extracted from my computer.

To create the layer in aws lambda it is necessary to create the package (.zip) with the following command 'zip -r pg.zip ./ruby/ ./lib/'.

This layer was built for the ruby-2.5.0 runtime using version 1.1.3 of the 'pg' gem and is expected to be used with Postgres 11.

To use the new_connection method it is necessary to pass as params. a hash like the following:
  {'host' => host, 'database' => database, 'username' => username, 'password' => password}

Important: In the lambda function configuration it is necessary to overwrite the environment variable GEM_PATH with '/opt/ruby/2.5.0'.
See more at: https://medium.com/devopslinks/how-to-use-aws-lambda-layers-f4fe6624aff1



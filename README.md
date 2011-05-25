mod_global_roster
=================

%% Compile
erlc -I /Path/to/ejabberd/src/ src/mod_global_roster.erl

%% mv .beam to /lib/ejabberd/ebin

%% Add mobule to ejabberd.cfg
  
  {mod_global_roster, [{key, "roster:", redis_host, "0.0.0.0", redis_port, 6379, redis_db, 0}]}

%% Options above are defaults, overwrite for custom options.

%% Start ejabberd

%% Note eredis is a dependancy and needs to be in your code path

%% Install eredis
git clone https://github.com/wooga/eredis.git

cd eredis

./rebar compile

%% (ln all files in ebin to /lib/ejabberd/ebin)

%% TODO Erlang/ejabberd versions needed

%% Install ejabberd full

git clone https://github.com/processone/ejabberd.git

cd ejabberd

git checkout -b 2.1.x origin/2.1.x

cd src

./configure (add path?)

make

sudo make install

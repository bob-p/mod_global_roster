mod_global_roster

%% Compile
erlc -I /Path/to/ejabberd/src/ src/mod_global_roster.erl

%% mv .beam to /lib/ejabberd/ebin

%% Add mobule to ejabberd.cfg
  {mod_global_roster, [{key, "roster:", redis_host, "1.1.1.1", redis_port, 6379, redis_db, 0}]}

%% Options above are defaults, overwrite for custom options.

%% Start ejabberd

%% Note eredis is a dependancy and needs to be in your code path (/lib/ejabberd/ebin)

%% TODO Erlang/ejabberd versions needed

%% Install ejabberd full

git clone https://github.com/processone/ejabberd.git
cd ejabberd
git checkout -b 2.1.x origin/2.1.x
cd src
./configure (add path?)
make
sudo make install

# munin-sidekiq_stats

![munin-sidekiq_stats example](https://raw.githubusercontent.com/t-cyrill/munin-sidekiq_stats/master/images/example.png "munin-sidekiq_stats example")

A munin plugin for Linux to monitor sidekiq (Ruby job worker) stats

Usage
----------------

Copy `_sidekiq_stats` to munin plugins directory. (i.e. /usr/share/munin/plugins)

And create symbolic link with application name prefix.

```
ln -s /usr/share/munin/plugins/_sidekiq_stats /etc/munin/plugins/example-app_sidekiq_stats
```

Create munin configration.

### Example

```
[example-app_sidekiq_stats]
  user app_user
  env.APP_NAME example-app
  env.RAILS_ROOT /var/www/example-app/current
```

Restart munin-node.

```
sudo /etc/init.d/munin-node restart
```

## Contributing

1. Fork it ( http://github.com/t-cyrill/munin-sidekiq_stats/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

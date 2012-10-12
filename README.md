#Dickens

`gem install dickens`

## SDCV installation
### Linux

```sh
  sudo apt-get install sdcv
```

### MacOS
In Mac OS it is possible to install SDCV using Ports:

```sh
  port install sdcv
```

### Dictionaries
Lots of dics may be found across the net. The starting point may be (here)[http://www.stardict.org/download.php]
#### Install dictionaries on Linux

```sh
  tar -xjvf a.tar.bz2
  mv a /usr/share/stardict/dic
```

## API methods
### List
After everything is installed you can list the dictionaries:

```ruby
  Dickens::StarDict.list
```

### Find
You can lookup desired definition through all dics at once:

```ruby
  Dickens::StarDict.find("Dickens")
```

### Where
Define dictionaries to lookup only inside those dics:
```ruby
  list=Dickens::StarDict.list
  Dickens::StarDict.where("Dickens", [list[1], list[3]])
```

### Configuration
Change the path to executable:
```ruby
  Dickens::StarDict.executable = "./lib/my_sdcv"
```

Control your options
```ruby
  Dickens::StarDict.config :use_dict => false,
                           :utf8_input => true,
                           :utf8_output => true,
                           :non_interactive => true,
                           :data_dir=>false
```



<div align="center">

# laravel.nvim

A lightweight, no-frills Neovim plugin that automatically detects Laravel projects and adds a :Laravel command for easy access to Artisan and Composer tasks. Perfect for keeping things simple and staying focused on code without extra setup or navigation.

</div>

## ⚡ Requirements

- Neovim 0.8+

## 📦 Installation

laravel.nvim supports all the usual plugin managers

<details open>
  <summary><a href="https://github.com/folke/lazy.nvim">🔗</a> lazy.nvim</summary>

```lua
{
  "djaruun/laravel.nvim",
  config = true,
}
```
</details>

## 🔌 Quick start

<details>
<summary>Full config example for lazy.nvim</summary>

```lua
{
  "djaruun/laravel.nvim",
  config = true,
}
```
</details>

## 🚀 Usage

In Laravel projects, do `:Laravel` and then your favorite `php artisan` command. It supports `php artisan` commands at the top-level and namespaces `composer` commands under `composer:`.

#### Example of starting the dev server using composer's dev script:

`:Laravel composer:dev`

#### The same example using artisan's serve:

`:Laravel serve`

#### Example of generating a component:

`:Laravel make:component Button`

## 🔧 Configuration

At the moment there is no configuration options available. It should just work out of the box.
If there are any options you would like or it doesn't work like it should, please feel free open an issue in the repository!

## Technical overview

Basically, all it does is run `term php artisan <command>` or `term composer <command>` for you and generates command completions from the available commands from `artisan` and `composer` using `<php artisan/composer> list --format=json --short`.

## 💫 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=djaruun/laravel.nvim&type=Date&theme=dark)](https://star-history.com/#djaruun/laravel.nvim&Date)

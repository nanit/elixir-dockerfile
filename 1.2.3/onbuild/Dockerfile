FROM nanit/elixir:1.2.3
MAINTAINER Erez Rabih

RUN mkdir -p /usr/app/src

ENV MIX_ENV prod
WORKDIR /usr/app/src
#Cache dependencies
ONBUILD COPY mix.exs /usr/app/src
ONBUILD COPY mix.lock /usr/app/src
#
ONBUILD RUN mix deps.get

ONBUILD COPY . /usr/app/src

ONBUILD RUN mix compile

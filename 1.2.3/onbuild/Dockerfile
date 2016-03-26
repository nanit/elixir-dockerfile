FROM nanit/elixir:1.2.3
MAINTAINER Erez Rabih

RUN mkdir -p /usr/app/src

ENV MIX_ENV prod
WORKDIR /usr/app/src
#Cache dependencies
COPY mix.exs /usr/app/src
COPY mix.lock /usr/app/src
#
RUN mix deps.get

COPY . /usr/app/src

RUN mix compile

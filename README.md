我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

argo/rpc
====

[![Go Report Card](https://goreportcard.com/badge/github.com/zyxar/argo)](https://goreportcard.com/report/github.com/zyxar/argo)
[![GoDoc](https://godoc.org/github.com/zyxar/argo/rpc?status.svg)](https://godoc.org/github.com/zyxar/argo/rpc)
[![Build Status](https://travis-ci.org/zyxar/argo.svg?branch=master)](https://travis-ci.org/zyxar/argo)

aria2 RPC in #Go


## Install

`go get github.com/zyxar/argo/rpc`


## Interface

```go
  AddURI(uri string, options ...interface{}) (gid string, err error)
  AddTorrent(filename string, options ...interface{}) (gid string, err error)
  AddMetalink(uri string, options ...interface{}) (gid string, err error)
  Remove(gid string) (msg string, err error)
  ForceRemove(gid string) (msg string, err error)
  Pause(gid string) (msg string, err error)
  PauseAll() (msg string, err error)
  ForcePause(gid string) (msg string, err error)
  ForcePauseAll() (msg string, err error)
  Unpause(gid string) (msg string, err error)
  UnpauseAll() (msg string, err error)
  TellStatus(gid string, keys ...string) (o Option, err error)
  GetUris(gid string) (o Option, err error)
  GetFiles(gid string) (o Option, err error)
  GetPeers(gid string) (o []Option, err error)
  GetServers(gid string) (o []Option, err error)
  TellActive(keys ...string) (o []Option, err error)
  TellWaiting(offset, num int, keys ...string) (o []Option, err error)
  TellStopped(offset, num int, keys ...string) (o []Option, err error)
  ChangePosition(gid string, pos int, how string) (p int, err error)
  ChangeURI(gid string, fileindex int, delUris []string, addUris []string, position ...int) (p []int, err error)
  GetOption(gid string) (o Option, err error)
  ChangeOption(gid string, options Option) (msg string, err error)
  GetGlobalOption() (o Option, err error)
  ChangeGlobalOption(options Option) (msg string, err error)
  GetGlobalStat() (o Option, err error)
  PurgeDowloadResult() (msg string, err error)
  RemoveDownloadResult(gid string) (msg string, err error)
  GetVersion() (o Option, err error)
  GetSessionInfo() (o Option, err error)
  Shutdown() (msg string, err error)
  ForceShutdown() (msg string, err error)
  Multicall(methods []Option) (r []interface{}, err error)
```

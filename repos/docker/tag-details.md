<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:19`](#docker19)
-	[`docker:19-dind`](#docker19-dind)
-	[`docker:19-dind-rootless`](#docker19-dind-rootless)
-	[`docker:19-git`](#docker19-git)
-	[`docker:19.03`](#docker1903)
-	[`docker:19.03-dind`](#docker1903-dind)
-	[`docker:19.03-dind-rootless`](#docker1903-dind-rootless)
-	[`docker:19.03-git`](#docker1903-git)
-	[`docker:19.03.15`](#docker190315)
-	[`docker:19.03.15-dind`](#docker190315-dind)
-	[`docker:19.03.15-dind-rootless`](#docker190315-dind-rootless)
-	[`docker:19.03.15-git`](#docker190315-git)
-	[`docker:20`](#docker20)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10.5`](#docker20105)
-	[`docker:20.10.5-dind`](#docker20105-dind)
-	[`docker:20.10.5-dind-rootless`](#docker20105-dind-rootless)
-	[`docker:20.10.5-git`](#docker20105-git)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)

## `docker:19`

```console
$ docker pull docker@sha256:894ecb10e963b838bd0af0bd487c4f4b4354ce035e154df275e2e019ed2a98d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19` - linux; amd64

```console
$ docker pull docker@sha256:9818e61e85e55ae756eb5e2dd9ad28adcc61329bdace10e6464fba8f973c2514
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67746947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b9af0261d8f37ffb268e19266399051b5d383d87de9267a31e666dd42d7b04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v6

```console
$ docker pull docker@sha256:18d39b6848cecae067cc0d94c554029bfc88d3069c80bb5049d54da659249b94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3106fcafb44a465ee4e0efadc103e5018d57587bd5d5ba6f465846bf7c3844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce46ea18798c578f8923e0ced4c9996c30363fc35edd1b1c40e5e542407818ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a685736103d7a1e988f52fb20b130a353e545dff4ccd52c9b075d5ead6f11d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:74f5fd7b268452f167f2c066a6fca7d1663f32f0e04bcd1cf1283f9499f6fbed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60766006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f972e043ccbaf098c06050ff11e1c01fbbdf571973eed0b78915410e91b48ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind`

```console
$ docker pull docker@sha256:a20300a53246e7a7c0d7fcebc79e29313809aea2b03dd42d47d81a6f314c1eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-dind` - linux; amd64

```console
$ docker pull docker@sha256:fcce60ebd97400dac9185d07168d2b994632e3531c0955784e9d161e36ee1231
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74321402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b61e8e087ad9b708087eb6d49bb8284fca4f05625c252f3145de9c1a66645e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6b0193cbf4d3c304f3bf6c6c253d88c25a22c6ffe6847fd57a6269e4324745f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a37c38067d51b4185a04675f81f45209b82449ce8bbbec68b31d639ba45cd5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 23 Apr 2020 17:13:24 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 23 Apr 2020 17:13:25 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 23 Apr 2020 17:13:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:49:37 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:49:38 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:49:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:49:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:49:39 GMT
CMD []
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0227df4100f67814d05f04e139a5e9dca37299fd9d096c7574e16fe632211d4`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 3.2 MB (3160940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2483e804c9900710b0cfa9c5cad284336a14d95ec28dc1049dc1b3cc10de4`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906e300d3ad75b25c6513f466d68c5a2dc89ce9663dd6526821b9994ceef549`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd819080e27b055eaa67e449dc1475fa02b89c7eb8406d4fd558c817df9ea`  
		Last Modified: Wed, 06 May 2020 00:50:04 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f998921d365053bf7e3f98794f6c23ca44e6809832d78105bc4d2da6bb8521ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220c6648aa1a61c12d4f11dd3c99b4385828e8c4d9823a5656f4f40294c1d41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 02:04:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 02:04:18 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 02:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:57:36 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:57:37 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:57:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:57:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:57:39 GMT
CMD []
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec2c432e5c5b4a7f698ed4b9ae252a67bf63604d41a06f871228065ded28a0`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.8 MB (2824842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c0882dce0c322a151afe082f0005164734b3df8b685891a1796351c2c8155`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c8f90da7135b8a7bd1382287287fc0a77f5671a336d4e82b2d9bd7bfee975`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7687b9e4e3e2a29a9e10fda7c4e188a5f92507110c037afc83048a374ebb7`  
		Last Modified: Wed, 06 May 2020 00:58:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cfa6db10c8be33c394543b867a8570410bce4db7de2a3e51d21974f28d89e7a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67243864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d780c340ea7f5eebfede12d370aa3a9aed14b93dcf61351b476dae7e9832d777`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:20:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:20:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:20:12 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:20:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:20:17 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:20:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:20:18 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:20:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:20 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb638e8d47f306670b8f2bfa21b840f8030212065fc5ba78b8f955086037786d`  
		Last Modified: Thu, 01 Apr 2021 13:22:20 GMT  
		Size: 6.5 MB (6473106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1999e812188fad271d75299091f16e799b629aa37feca6b8df4de9f676d14477`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f408828fd423e20ed50dbe48fd9c77e100a0b6a4eb68d6723222894235ab9`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62f5160ccacd11650844620724688941736aafd51f6fc3a26867de636f1576c`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:8023ef461c8b507f4049df73998298289c2ac3d510aca76bac8374a2911f9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c2fa5d15f05b13d51fcfd194fe336452d156baa2fe74a93d672ab9ee9d4aa198
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94877362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab1ae720603cdb1e92789a7fd95e3bec04c74a2a4835634e512ad63649191bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
# Thu, 01 Apr 2021 14:01:03 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:01:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:01:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:01:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:01:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:01:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e73dbffe5a55fe14967bdd47a418c821712f5952da8f4d45f10450c5ce6f3f`  
		Last Modified: Thu, 01 Apr 2021 14:04:12 GMT  
		Size: 1.1 MB (1131563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2c536df88aa50d092aa553e47f1e6daa72adf9d20105d6c61283253c7ae118`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b5ea595ed45305d464afbc3aa04fc621eb6dbf3ae0aa6057091d6472fffd97`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e337b6f794aa5bf5b618857d55b2314dde080241106ecced70fa0cb285334a`  
		Last Modified: Thu, 01 Apr 2021 14:04:15 GMT  
		Size: 19.4 MB (19422690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0dad659d908561f0ad90d499aa0957876110fe95caca7a46e44905b3316ba3`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-git`

```console
$ docker pull docker@sha256:b9e9520c417d89b14288872d78b79c845f7d690c3a7d406ab09f669fda1ad5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-git` - linux; amd64

```console
$ docker pull docker@sha256:4fa61b5897f7ca5ff04247aeed1b5928fe8d54ead71edb47e45d3475046e810b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74139750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b0f74f103fd1d7a0b0273ffe95cfb6e619861d35efab4c24613b62d0960b23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:01:14 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f882db0cfbe4dfc4913c63a5b5b05102cd3418c6a9ce4ea2b271c76469f506`  
		Last Modified: Thu, 01 Apr 2021 14:04:35 GMT  
		Size: 6.4 MB (6392803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:e89d2f422796bb472a3f6c301076f8f64fb9f6c3078ff96a8cc7918121a9130f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba101ef968406449d45b9bf5373293c6f08f400cea9e947b6158777032233591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b175115645c91b877c5783ddd6faf72ccddb1584eabd8187f8f8def8c2e17`  
		Last Modified: Fri, 24 Apr 2020 02:05:44 GMT  
		Size: 7.0 MB (7031330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e4a77a1db29a9467481e365d9b448c7ba2267c8f13e4bf376688a6c7ae88cf97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67241812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e39c636516f9344aa9cc4e68a36c8bfd309713c9c2edcd2018ca791b12163eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:20:31 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072f23b6a66272d9eacbad5d2467d4859d01dcb047236a3a0dd709c7e077565e`  
		Last Modified: Thu, 01 Apr 2021 13:22:30 GMT  
		Size: 6.5 MB (6475806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03`

```console
$ docker pull docker@sha256:894ecb10e963b838bd0af0bd487c4f4b4354ce035e154df275e2e019ed2a98d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03` - linux; amd64

```console
$ docker pull docker@sha256:9818e61e85e55ae756eb5e2dd9ad28adcc61329bdace10e6464fba8f973c2514
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67746947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b9af0261d8f37ffb268e19266399051b5d383d87de9267a31e666dd42d7b04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v6

```console
$ docker pull docker@sha256:18d39b6848cecae067cc0d94c554029bfc88d3069c80bb5049d54da659249b94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3106fcafb44a465ee4e0efadc103e5018d57587bd5d5ba6f465846bf7c3844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce46ea18798c578f8923e0ced4c9996c30363fc35edd1b1c40e5e542407818ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a685736103d7a1e988f52fb20b130a353e545dff4ccd52c9b075d5ead6f11d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:74f5fd7b268452f167f2c066a6fca7d1663f32f0e04bcd1cf1283f9499f6fbed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60766006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f972e043ccbaf098c06050ff11e1c01fbbdf571973eed0b78915410e91b48ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind`

```console
$ docker pull docker@sha256:a20300a53246e7a7c0d7fcebc79e29313809aea2b03dd42d47d81a6f314c1eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-dind` - linux; amd64

```console
$ docker pull docker@sha256:fcce60ebd97400dac9185d07168d2b994632e3531c0955784e9d161e36ee1231
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74321402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b61e8e087ad9b708087eb6d49bb8284fca4f05625c252f3145de9c1a66645e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6b0193cbf4d3c304f3bf6c6c253d88c25a22c6ffe6847fd57a6269e4324745f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a37c38067d51b4185a04675f81f45209b82449ce8bbbec68b31d639ba45cd5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 23 Apr 2020 17:13:24 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 23 Apr 2020 17:13:25 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 23 Apr 2020 17:13:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:49:37 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:49:38 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:49:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:49:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:49:39 GMT
CMD []
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0227df4100f67814d05f04e139a5e9dca37299fd9d096c7574e16fe632211d4`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 3.2 MB (3160940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2483e804c9900710b0cfa9c5cad284336a14d95ec28dc1049dc1b3cc10de4`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906e300d3ad75b25c6513f466d68c5a2dc89ce9663dd6526821b9994ceef549`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd819080e27b055eaa67e449dc1475fa02b89c7eb8406d4fd558c817df9ea`  
		Last Modified: Wed, 06 May 2020 00:50:04 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f998921d365053bf7e3f98794f6c23ca44e6809832d78105bc4d2da6bb8521ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220c6648aa1a61c12d4f11dd3c99b4385828e8c4d9823a5656f4f40294c1d41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 02:04:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 02:04:18 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 02:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:57:36 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:57:37 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:57:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:57:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:57:39 GMT
CMD []
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec2c432e5c5b4a7f698ed4b9ae252a67bf63604d41a06f871228065ded28a0`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.8 MB (2824842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c0882dce0c322a151afe082f0005164734b3df8b685891a1796351c2c8155`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c8f90da7135b8a7bd1382287287fc0a77f5671a336d4e82b2d9bd7bfee975`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7687b9e4e3e2a29a9e10fda7c4e188a5f92507110c037afc83048a374ebb7`  
		Last Modified: Wed, 06 May 2020 00:58:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cfa6db10c8be33c394543b867a8570410bce4db7de2a3e51d21974f28d89e7a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67243864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d780c340ea7f5eebfede12d370aa3a9aed14b93dcf61351b476dae7e9832d777`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:20:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:20:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:20:12 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:20:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:20:17 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:20:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:20:18 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:20:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:20 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb638e8d47f306670b8f2bfa21b840f8030212065fc5ba78b8f955086037786d`  
		Last Modified: Thu, 01 Apr 2021 13:22:20 GMT  
		Size: 6.5 MB (6473106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1999e812188fad271d75299091f16e799b629aa37feca6b8df4de9f676d14477`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f408828fd423e20ed50dbe48fd9c77e100a0b6a4eb68d6723222894235ab9`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62f5160ccacd11650844620724688941736aafd51f6fc3a26867de636f1576c`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind-rootless`

```console
$ docker pull docker@sha256:8023ef461c8b507f4049df73998298289c2ac3d510aca76bac8374a2911f9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c2fa5d15f05b13d51fcfd194fe336452d156baa2fe74a93d672ab9ee9d4aa198
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94877362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab1ae720603cdb1e92789a7fd95e3bec04c74a2a4835634e512ad63649191bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
# Thu, 01 Apr 2021 14:01:03 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:01:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:01:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:01:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:01:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:01:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e73dbffe5a55fe14967bdd47a418c821712f5952da8f4d45f10450c5ce6f3f`  
		Last Modified: Thu, 01 Apr 2021 14:04:12 GMT  
		Size: 1.1 MB (1131563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2c536df88aa50d092aa553e47f1e6daa72adf9d20105d6c61283253c7ae118`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b5ea595ed45305d464afbc3aa04fc621eb6dbf3ae0aa6057091d6472fffd97`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e337b6f794aa5bf5b618857d55b2314dde080241106ecced70fa0cb285334a`  
		Last Modified: Thu, 01 Apr 2021 14:04:15 GMT  
		Size: 19.4 MB (19422690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0dad659d908561f0ad90d499aa0957876110fe95caca7a46e44905b3316ba3`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-git`

```console
$ docker pull docker@sha256:b9e9520c417d89b14288872d78b79c845f7d690c3a7d406ab09f669fda1ad5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-git` - linux; amd64

```console
$ docker pull docker@sha256:4fa61b5897f7ca5ff04247aeed1b5928fe8d54ead71edb47e45d3475046e810b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74139750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b0f74f103fd1d7a0b0273ffe95cfb6e619861d35efab4c24613b62d0960b23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:01:14 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f882db0cfbe4dfc4913c63a5b5b05102cd3418c6a9ce4ea2b271c76469f506`  
		Last Modified: Thu, 01 Apr 2021 14:04:35 GMT  
		Size: 6.4 MB (6392803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:e89d2f422796bb472a3f6c301076f8f64fb9f6c3078ff96a8cc7918121a9130f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba101ef968406449d45b9bf5373293c6f08f400cea9e947b6158777032233591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b175115645c91b877c5783ddd6faf72ccddb1584eabd8187f8f8def8c2e17`  
		Last Modified: Fri, 24 Apr 2020 02:05:44 GMT  
		Size: 7.0 MB (7031330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e4a77a1db29a9467481e365d9b448c7ba2267c8f13e4bf376688a6c7ae88cf97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67241812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e39c636516f9344aa9cc4e68a36c8bfd309713c9c2edcd2018ca791b12163eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:20:31 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072f23b6a66272d9eacbad5d2467d4859d01dcb047236a3a0dd709c7e077565e`  
		Last Modified: Thu, 01 Apr 2021 13:22:30 GMT  
		Size: 6.5 MB (6475806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.15`

```console
$ docker pull docker@sha256:c3aeb14b6a54952030a2246eea62aac27ee959cc45354d41e671174fd9c76efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:19.03.15` - linux; amd64

```console
$ docker pull docker@sha256:9818e61e85e55ae756eb5e2dd9ad28adcc61329bdace10e6464fba8f973c2514
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67746947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b9af0261d8f37ffb268e19266399051b5d383d87de9267a31e666dd42d7b04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:74f5fd7b268452f167f2c066a6fca7d1663f32f0e04bcd1cf1283f9499f6fbed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60766006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f972e043ccbaf098c06050ff11e1c01fbbdf571973eed0b78915410e91b48ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.15-dind`

```console
$ docker pull docker@sha256:5c7d7e28a885c6468a67ae6523d1ff77653b3100c5f645f6124385ed72d14f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:19.03.15-dind` - linux; amd64

```console
$ docker pull docker@sha256:fcce60ebd97400dac9185d07168d2b994632e3531c0955784e9d161e36ee1231
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74321402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b61e8e087ad9b708087eb6d49bb8284fca4f05625c252f3145de9c1a66645e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.15-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cfa6db10c8be33c394543b867a8570410bce4db7de2a3e51d21974f28d89e7a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67243864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d780c340ea7f5eebfede12d370aa3a9aed14b93dcf61351b476dae7e9832d777`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:20:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:20:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:20:12 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:20:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:20:17 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:20:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:20:18 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:20:19 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:20 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb638e8d47f306670b8f2bfa21b840f8030212065fc5ba78b8f955086037786d`  
		Last Modified: Thu, 01 Apr 2021 13:22:20 GMT  
		Size: 6.5 MB (6473106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1999e812188fad271d75299091f16e799b629aa37feca6b8df4de9f676d14477`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f408828fd423e20ed50dbe48fd9c77e100a0b6a4eb68d6723222894235ab9`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62f5160ccacd11650844620724688941736aafd51f6fc3a26867de636f1576c`  
		Last Modified: Thu, 01 Apr 2021 13:22:19 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.15-dind-rootless`

```console
$ docker pull docker@sha256:8023ef461c8b507f4049df73998298289c2ac3d510aca76bac8374a2911f9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.15-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c2fa5d15f05b13d51fcfd194fe336452d156baa2fe74a93d672ab9ee9d4aa198
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94877362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab1ae720603cdb1e92789a7fd95e3bec04c74a2a4835634e512ad63649191bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
# Thu, 01 Apr 2021 14:01:03 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:01:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:01:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:01:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:01:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:01:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e73dbffe5a55fe14967bdd47a418c821712f5952da8f4d45f10450c5ce6f3f`  
		Last Modified: Thu, 01 Apr 2021 14:04:12 GMT  
		Size: 1.1 MB (1131563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2c536df88aa50d092aa553e47f1e6daa72adf9d20105d6c61283253c7ae118`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b5ea595ed45305d464afbc3aa04fc621eb6dbf3ae0aa6057091d6472fffd97`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e337b6f794aa5bf5b618857d55b2314dde080241106ecced70fa0cb285334a`  
		Last Modified: Thu, 01 Apr 2021 14:04:15 GMT  
		Size: 19.4 MB (19422690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0dad659d908561f0ad90d499aa0957876110fe95caca7a46e44905b3316ba3`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.15-git`

```console
$ docker pull docker@sha256:8dbc5e4c1a46076623c9b09ae0a58321b2c6d27cb233e498f258968a7eae2c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:19.03.15-git` - linux; amd64

```console
$ docker pull docker@sha256:4fa61b5897f7ca5ff04247aeed1b5928fe8d54ead71edb47e45d3475046e810b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74139750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b0f74f103fd1d7a0b0273ffe95cfb6e619861d35efab4c24613b62d0960b23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:01:14 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f882db0cfbe4dfc4913c63a5b5b05102cd3418c6a9ce4ea2b271c76469f506`  
		Last Modified: Thu, 01 Apr 2021 14:04:35 GMT  
		Size: 6.4 MB (6392803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.15-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e4a77a1db29a9467481e365d9b448c7ba2267c8f13e4bf376688a6c7ae88cf97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67241812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e39c636516f9344aa9cc4e68a36c8bfd309713c9c2edcd2018ca791b12163eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:19:41 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 13:19:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:19:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:19:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:19:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:58 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:20:31 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba513d4de3d6302e8fbb3e68e4a320c0a29e98d069c1f334cd645fba53191269`  
		Last Modified: Thu, 01 Apr 2021 13:22:09 GMT  
		Size: 56.0 MB (55994346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066980b1248090af64623ce97cc1a6a83556ee3b14bcafceaaae464ce55c4e8d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d19192ae857018cc22f0fec3c7bed03252686fc678f382071f5a41d0d2222d`  
		Last Modified: Thu, 01 Apr 2021 13:21:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72832def30b05fc9b1b614469ce7a4644d2cfa877d682dc483e895ff2a80555`  
		Last Modified: Thu, 01 Apr 2021 13:21:54 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072f23b6a66272d9eacbad5d2467d4859d01dcb047236a3a0dd709c7e077565e`  
		Last Modified: Thu, 01 Apr 2021 13:22:30 GMT  
		Size: 6.5 MB (6475806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20`

```console
$ docker pull docker@sha256:7ed427295687586039ff3433bb9b4419c5cf1e6294025dadf7641126665a78f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:ab80379593592baff0c7594eea95f40654ab6e92dd1983f012e51541f59aed8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74556151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:72c2830c5e0823d3140db951e0d17bebf853e07105596b46555e00e1f02eb0da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68548448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd38dbb5fc575e2667c6c5e443b020b12a20e3e827a1284d8a8aa2c40a069a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:e4ecd4e9ad5140d584669451b05e406d8cf7603e51972b862178ad93c38b2b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:06e758ed285b2f06c66b435b213af33e0e3bd5a4d9333ce7028d73c1861c59c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9822c8848df3eb0a1562e553fdd54215939ef0a528434ee026c64ff645148c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dd7e83ac453a8b305e12b95ab96bf484f99e17864b9a3fca3b1e1cf63abd6835
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75065855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e795a054747ec1ac6b0fbea90a8ba6df7f60fe5812ccd1354f5b816f0f6c82d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:19:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:19:13 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:19:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:19:18 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:19:19 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:19:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:22 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc45ae6a51b1626108430a9de3df3b52ea75b06549211efb1a03a4603faabb6`  
		Last Modified: Thu, 01 Apr 2021 13:21:31 GMT  
		Size: 6.5 MB (6512656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc1e6fda685d9c056d92a8791a3ad6bcba95a24559ce04a7159ae830e239c3`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ab3fb0455a7ba088581f80bf45bc129bd3dffcde348f69a3ddc8ae1f8efbdf`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809319b5617b2be0d0249b0bb3c9002e32a88154efe1359e03541fef6d89b00`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:00a23dee2c8bd6d818964102ff7f76d9a9fccc3a2127e4ff230627091b1811ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:473b20f9ad71196d60d334e3239cf71faf93041e8c58c93428f711b6f52ab9ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102536000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195378697290a5abbceac60a3d19ec0e7e201c1b23b869e3920c1e29bcab94e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
# Thu, 01 Apr 2021 14:00:28 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:00:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:00:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:00:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:00:33 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:00:33 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bedae01be2b43fb2d9345c1f55846386fb298c42ff5037e3b28c9255dbb40e`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.1 MB (1131817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f70ed8e03fc1baa16b02a9ac2d5dbd68aa0397de6c7ba44d1c584ad41a25f8`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4fd2f8a18f540cbeb06e404b9fb6e5f502d42b78e4165a8dad1d06c5a77d0a`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b978a36a14bc2a9d0fa3ec7c05ff0e0837a18e20dfeb98db711a4567ee24bded`  
		Last Modified: Thu, 01 Apr 2021 14:02:46 GMT  
		Size: 20.2 MB (20231015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f10dea2b0f01859d2e06a372e0c1b4429b1c18353fa22edfd50663a2f2c91ea`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:28e473065b42f54ecfccc0d84777a16e971ab628523736f24bb6e3b83c34890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:65a46b762db55ebc894b9f2d25114565c4435ee7c3d2433948ac7e5f2a12678c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80948983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20857e2d493719cde04da6183d772d4af62f77e58be13fa9f2da7b0410fdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:38 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200f3f4a506a8bf68892a66feb9d023930b3e910b62baaae5fcfb942c7bf3d55`  
		Last Modified: Thu, 01 Apr 2021 14:03:11 GMT  
		Size: 6.4 MB (6392832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a8ca53682290cf0a342ef42f5458905385619e2099e34d67959d842426ddcd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75024239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf59598d54119927f27ec71c136d3a901fbff352fd5f2b560a28c00bd4972a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:34 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3e1042215ed49358357c1951c9909d6fe8aabc3769b9442d75469aad58b05`  
		Last Modified: Thu, 01 Apr 2021 13:21:43 GMT  
		Size: 6.5 MB (6475791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:7ed427295687586039ff3433bb9b4419c5cf1e6294025dadf7641126665a78f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:ab80379593592baff0c7594eea95f40654ab6e92dd1983f012e51541f59aed8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74556151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:72c2830c5e0823d3140db951e0d17bebf853e07105596b46555e00e1f02eb0da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68548448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd38dbb5fc575e2667c6c5e443b020b12a20e3e827a1284d8a8aa2c40a069a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:e4ecd4e9ad5140d584669451b05e406d8cf7603e51972b862178ad93c38b2b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:06e758ed285b2f06c66b435b213af33e0e3bd5a4d9333ce7028d73c1861c59c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9822c8848df3eb0a1562e553fdd54215939ef0a528434ee026c64ff645148c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dd7e83ac453a8b305e12b95ab96bf484f99e17864b9a3fca3b1e1cf63abd6835
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75065855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e795a054747ec1ac6b0fbea90a8ba6df7f60fe5812ccd1354f5b816f0f6c82d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:19:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:19:13 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:19:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:19:18 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:19:19 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:19:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:22 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc45ae6a51b1626108430a9de3df3b52ea75b06549211efb1a03a4603faabb6`  
		Last Modified: Thu, 01 Apr 2021 13:21:31 GMT  
		Size: 6.5 MB (6512656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc1e6fda685d9c056d92a8791a3ad6bcba95a24559ce04a7159ae830e239c3`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ab3fb0455a7ba088581f80bf45bc129bd3dffcde348f69a3ddc8ae1f8efbdf`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809319b5617b2be0d0249b0bb3c9002e32a88154efe1359e03541fef6d89b00`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:00a23dee2c8bd6d818964102ff7f76d9a9fccc3a2127e4ff230627091b1811ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:473b20f9ad71196d60d334e3239cf71faf93041e8c58c93428f711b6f52ab9ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102536000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195378697290a5abbceac60a3d19ec0e7e201c1b23b869e3920c1e29bcab94e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
# Thu, 01 Apr 2021 14:00:28 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:00:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:00:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:00:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:00:33 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:00:33 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bedae01be2b43fb2d9345c1f55846386fb298c42ff5037e3b28c9255dbb40e`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.1 MB (1131817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f70ed8e03fc1baa16b02a9ac2d5dbd68aa0397de6c7ba44d1c584ad41a25f8`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4fd2f8a18f540cbeb06e404b9fb6e5f502d42b78e4165a8dad1d06c5a77d0a`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b978a36a14bc2a9d0fa3ec7c05ff0e0837a18e20dfeb98db711a4567ee24bded`  
		Last Modified: Thu, 01 Apr 2021 14:02:46 GMT  
		Size: 20.2 MB (20231015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f10dea2b0f01859d2e06a372e0c1b4429b1c18353fa22edfd50663a2f2c91ea`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:28e473065b42f54ecfccc0d84777a16e971ab628523736f24bb6e3b83c34890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:65a46b762db55ebc894b9f2d25114565c4435ee7c3d2433948ac7e5f2a12678c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80948983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20857e2d493719cde04da6183d772d4af62f77e58be13fa9f2da7b0410fdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:38 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200f3f4a506a8bf68892a66feb9d023930b3e910b62baaae5fcfb942c7bf3d55`  
		Last Modified: Thu, 01 Apr 2021 14:03:11 GMT  
		Size: 6.4 MB (6392832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a8ca53682290cf0a342ef42f5458905385619e2099e34d67959d842426ddcd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75024239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf59598d54119927f27ec71c136d3a901fbff352fd5f2b560a28c00bd4972a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:34 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3e1042215ed49358357c1951c9909d6fe8aabc3769b9442d75469aad58b05`  
		Last Modified: Thu, 01 Apr 2021 13:21:43 GMT  
		Size: 6.5 MB (6475791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.5`

```console
$ docker pull docker@sha256:7ed427295687586039ff3433bb9b4419c5cf1e6294025dadf7641126665a78f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.5` - linux; amd64

```console
$ docker pull docker@sha256:ab80379593592baff0c7594eea95f40654ab6e92dd1983f012e51541f59aed8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74556151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:72c2830c5e0823d3140db951e0d17bebf853e07105596b46555e00e1f02eb0da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68548448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd38dbb5fc575e2667c6c5e443b020b12a20e3e827a1284d8a8aa2c40a069a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.5-dind`

```console
$ docker pull docker@sha256:e4ecd4e9ad5140d584669451b05e406d8cf7603e51972b862178ad93c38b2b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:06e758ed285b2f06c66b435b213af33e0e3bd5a4d9333ce7028d73c1861c59c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9822c8848df3eb0a1562e553fdd54215939ef0a528434ee026c64ff645148c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dd7e83ac453a8b305e12b95ab96bf484f99e17864b9a3fca3b1e1cf63abd6835
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75065855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e795a054747ec1ac6b0fbea90a8ba6df7f60fe5812ccd1354f5b816f0f6c82d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:19:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:19:13 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:19:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:19:18 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:19:19 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:19:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:22 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc45ae6a51b1626108430a9de3df3b52ea75b06549211efb1a03a4603faabb6`  
		Last Modified: Thu, 01 Apr 2021 13:21:31 GMT  
		Size: 6.5 MB (6512656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc1e6fda685d9c056d92a8791a3ad6bcba95a24559ce04a7159ae830e239c3`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ab3fb0455a7ba088581f80bf45bc129bd3dffcde348f69a3ddc8ae1f8efbdf`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809319b5617b2be0d0249b0bb3c9002e32a88154efe1359e03541fef6d89b00`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.5-dind-rootless`

```console
$ docker pull docker@sha256:00a23dee2c8bd6d818964102ff7f76d9a9fccc3a2127e4ff230627091b1811ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20.10.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:473b20f9ad71196d60d334e3239cf71faf93041e8c58c93428f711b6f52ab9ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102536000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195378697290a5abbceac60a3d19ec0e7e201c1b23b869e3920c1e29bcab94e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
# Thu, 01 Apr 2021 14:00:28 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:00:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:00:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:00:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:00:33 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:00:33 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bedae01be2b43fb2d9345c1f55846386fb298c42ff5037e3b28c9255dbb40e`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.1 MB (1131817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f70ed8e03fc1baa16b02a9ac2d5dbd68aa0397de6c7ba44d1c584ad41a25f8`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4fd2f8a18f540cbeb06e404b9fb6e5f502d42b78e4165a8dad1d06c5a77d0a`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b978a36a14bc2a9d0fa3ec7c05ff0e0837a18e20dfeb98db711a4567ee24bded`  
		Last Modified: Thu, 01 Apr 2021 14:02:46 GMT  
		Size: 20.2 MB (20231015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f10dea2b0f01859d2e06a372e0c1b4429b1c18353fa22edfd50663a2f2c91ea`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.5-git`

```console
$ docker pull docker@sha256:28e473065b42f54ecfccc0d84777a16e971ab628523736f24bb6e3b83c34890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.5-git` - linux; amd64

```console
$ docker pull docker@sha256:65a46b762db55ebc894b9f2d25114565c4435ee7c3d2433948ac7e5f2a12678c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80948983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20857e2d493719cde04da6183d772d4af62f77e58be13fa9f2da7b0410fdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:38 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200f3f4a506a8bf68892a66feb9d023930b3e910b62baaae5fcfb942c7bf3d55`  
		Last Modified: Thu, 01 Apr 2021 14:03:11 GMT  
		Size: 6.4 MB (6392832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.5-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a8ca53682290cf0a342ef42f5458905385619e2099e34d67959d842426ddcd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75024239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf59598d54119927f27ec71c136d3a901fbff352fd5f2b560a28c00bd4972a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:34 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3e1042215ed49358357c1951c9909d6fe8aabc3769b9442d75469aad58b05`  
		Last Modified: Thu, 01 Apr 2021 13:21:43 GMT  
		Size: 6.5 MB (6475791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:8dd418f3a2ef4f5f83e6ed8f33ad21e9e9c3ce28baec1b8a06c95b2ef46cfdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:06e758ed285b2f06c66b435b213af33e0e3bd5a4d9333ce7028d73c1861c59c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9822c8848df3eb0a1562e553fdd54215939ef0a528434ee026c64ff645148c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6b0193cbf4d3c304f3bf6c6c253d88c25a22c6ffe6847fd57a6269e4324745f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a37c38067d51b4185a04675f81f45209b82449ce8bbbec68b31d639ba45cd5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 23 Apr 2020 17:13:24 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 23 Apr 2020 17:13:25 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 23 Apr 2020 17:13:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:49:37 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:49:38 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:49:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:49:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:49:39 GMT
CMD []
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0227df4100f67814d05f04e139a5e9dca37299fd9d096c7574e16fe632211d4`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 3.2 MB (3160940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a2483e804c9900710b0cfa9c5cad284336a14d95ec28dc1049dc1b3cc10de4`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906e300d3ad75b25c6513f466d68c5a2dc89ce9663dd6526821b9994ceef549`  
		Last Modified: Thu, 23 Apr 2020 17:14:36 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1dd819080e27b055eaa67e449dc1475fa02b89c7eb8406d4fd558c817df9ea`  
		Last Modified: Wed, 06 May 2020 00:50:04 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f998921d365053bf7e3f98794f6c23ca44e6809832d78105bc4d2da6bb8521ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220c6648aa1a61c12d4f11dd3c99b4385828e8c4d9823a5656f4f40294c1d41`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 02:04:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 02:04:18 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 02:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 06 May 2020 00:57:36 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Wed, 06 May 2020 00:57:37 GMT
VOLUME [/var/lib/docker]
# Wed, 06 May 2020 00:57:38 GMT
EXPOSE 2375 2376
# Wed, 06 May 2020 00:57:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 06 May 2020 00:57:39 GMT
CMD []
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec2c432e5c5b4a7f698ed4b9ae252a67bf63604d41a06f871228065ded28a0`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.8 MB (2824842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c0882dce0c322a151afe082f0005164734b3df8b685891a1796351c2c8155`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c8f90da7135b8a7bd1382287287fc0a77f5671a336d4e82b2d9bd7bfee975`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7687b9e4e3e2a29a9e10fda7c4e188a5f92507110c037afc83048a374ebb7`  
		Last Modified: Wed, 06 May 2020 00:58:02 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dd7e83ac453a8b305e12b95ab96bf484f99e17864b9a3fca3b1e1cf63abd6835
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75065855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e795a054747ec1ac6b0fbea90a8ba6df7f60fe5812ccd1354f5b816f0f6c82d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 13:19:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 13:19:13 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 13:19:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 13:19:18 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:19:18 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 13:19:19 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 13:19:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 13:19:22 GMT
CMD []
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc45ae6a51b1626108430a9de3df3b52ea75b06549211efb1a03a4603faabb6`  
		Last Modified: Thu, 01 Apr 2021 13:21:31 GMT  
		Size: 6.5 MB (6512656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc1e6fda685d9c056d92a8791a3ad6bcba95a24559ce04a7159ae830e239c3`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ab3fb0455a7ba088581f80bf45bc129bd3dffcde348f69a3ddc8ae1f8efbdf`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809319b5617b2be0d0249b0bb3c9002e32a88154efe1359e03541fef6d89b00`  
		Last Modified: Thu, 01 Apr 2021 13:21:30 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:00a23dee2c8bd6d818964102ff7f76d9a9fccc3a2127e4ff230627091b1811ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:473b20f9ad71196d60d334e3239cf71faf93041e8c58c93428f711b6f52ab9ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102536000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195378697290a5abbceac60a3d19ec0e7e201c1b23b869e3920c1e29bcab94e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:21 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:22 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:22 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:23 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:23 GMT
CMD []
# Thu, 01 Apr 2021 14:00:28 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:00:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:00:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:00:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:00:33 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:00:33 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc74ae0eadc2efb98a9862c135052a1c21776a5a8cb43c1022ecb4a69dddb0`  
		Last Modified: Thu, 01 Apr 2021 14:02:24 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738fafa691319a8faf0470e69146f25fd5d7a86e56741e7b8f7ec22f2d48b84`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0cc2e8bbf1b2f8f3db6d15b9fe6ff9e660da3496047060be8ebaf3873007`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac7bd276fd55d012fbce08352c662637823534bffad82ca80323caaf89755fa`  
		Last Modified: Thu, 01 Apr 2021 14:02:22 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bedae01be2b43fb2d9345c1f55846386fb298c42ff5037e3b28c9255dbb40e`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.1 MB (1131817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f70ed8e03fc1baa16b02a9ac2d5dbd68aa0397de6c7ba44d1c584ad41a25f8`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4fd2f8a18f540cbeb06e404b9fb6e5f502d42b78e4165a8dad1d06c5a77d0a`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b978a36a14bc2a9d0fa3ec7c05ff0e0837a18e20dfeb98db711a4567ee24bded`  
		Last Modified: Thu, 01 Apr 2021 14:02:46 GMT  
		Size: 20.2 MB (20231015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f10dea2b0f01859d2e06a372e0c1b4429b1c18353fa22edfd50663a2f2c91ea`  
		Last Modified: Thu, 01 Apr 2021 14:02:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:ac33954ae2c9f72e3d40af2b2c94867fe92a5d311f18afe51e55916441309976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:65a46b762db55ebc894b9f2d25114565c4435ee7c3d2433948ac7e5f2a12678c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80948983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20857e2d493719cde04da6183d772d4af62f77e58be13fa9f2da7b0410fdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:38 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200f3f4a506a8bf68892a66feb9d023930b3e910b62baaae5fcfb942c7bf3d55`  
		Last Modified: Thu, 01 Apr 2021 14:03:11 GMT  
		Size: 6.4 MB (6392832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v7

```console
$ docker pull docker@sha256:e89d2f422796bb472a3f6c301076f8f64fb9f6c3078ff96a8cc7918121a9130f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71205027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba101ef968406449d45b9bf5373293c6f08f400cea9e947b6158777032233591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 02:04:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2b175115645c91b877c5783ddd6faf72ccddb1584eabd8187f8f8def8c2e17`  
		Last Modified: Fri, 24 Apr 2020 02:05:44 GMT  
		Size: 7.0 MB (7031330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a8ca53682290cf0a342ef42f5458905385619e2099e34d67959d842426ddcd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75024239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf59598d54119927f27ec71c136d3a901fbff352fd5f2b560a28c00bd4972a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:34 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3e1042215ed49358357c1951c9909d6fe8aabc3769b9442d75469aad58b05`  
		Last Modified: Thu, 01 Apr 2021 13:21:43 GMT  
		Size: 6.5 MB (6475791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:0bc2c31bd4bf422f6e30a44449acb41e7c9bfd62bf9871504d482e26e12e94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:ab80379593592baff0c7594eea95f40654ab6e92dd1983f012e51541f59aed8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74556151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1588477122de4fdfe9fcb9ddeeee6ac6b93e9e05a65c68a6e22add0a98b8e0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:18d39b6848cecae067cc0d94c554029bfc88d3069c80bb5049d54da659249b94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3106fcafb44a465ee4e0efadc103e5018d57587bd5d5ba6f465846bf7c3844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:12:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 23 Apr 2020 17:12:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 17:12:50 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 23 Apr 2020 17:12:51 GMT
ENV DOCKER_VERSION=19.03.8
# Thu, 23 Apr 2020 17:13:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 23 Apr 2020 17:13:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 23 Apr 2020 17:13:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Apr 2020 17:13:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 23 Apr 2020 17:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcb342235c0ef85c7b7836ba057f513df540f983f4dbe5587035824aec248ab`  
		Last Modified: Thu, 23 Apr 2020 17:14:04 GMT  
		Size: 1.9 MB (1926703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94018ec82f0af1c26efba50dc99b07f2db1d2fbfab94f814ca9e1b5147c73e56`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e1c01de3a8ad095d83439f0112c9a534fe764682e7a0f99d0a5794f914591`  
		Last Modified: Thu, 23 Apr 2020 17:14:22 GMT  
		Size: 59.9 MB (59927152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3737124780efb66a0753c8acdb04e12dad9a04b3362b1496cfe1e1dcf2d60b`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a76f66eab7a2e5314dd5973bcbb4ab91a025072e77fd14a83ab87d5ed8cc39`  
		Last Modified: Thu, 23 Apr 2020 17:14:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e1037ca5d5c489e9b1a5f1433e4d8be4b012c29ef660e05769c63bfbd63812`  
		Last Modified: Thu, 23 Apr 2020 17:14:02 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce46ea18798c578f8923e0ced4c9996c30363fc35edd1b1c40e5e542407818ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a685736103d7a1e988f52fb20b130a353e545dff4ccd52c9b075d5ead6f11d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:03:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 02:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 02:03:47 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 02:03:48 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 02:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 02:04:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 02:04:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 02:04:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c2ce1bf627500ac9aec72c466865536bbff375e04a4e409655bbdf2827c1a`  
		Last Modified: Fri, 24 Apr 2020 02:04:53 GMT  
		Size: 1.8 MB (1822716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14a8989d4305a13a6c1fbfab29671cacd99035dd4291710ba978fd29283481`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b1f8e9eedb57e967305efe997babe0185ba6f7fe9eb7f4cbed6ee3d3f4dbe`  
		Last Modified: Fri, 24 Apr 2020 02:05:12 GMT  
		Size: 59.9 MB (59927054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc59092f5c3af9ff086a7203470a39d43b9ba5593cdd2eb494796a245ce8ecd4`  
		Last Modified: Fri, 24 Apr 2020 02:04:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f54a6c116900f095c4bce429f827a4dcc0af52c0634e42b3f83a9f5ea321d39`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb98a21ac35e0dd075007407e66183792d9dbc8c997513d6592918018b5312a`  
		Last Modified: Fri, 24 Apr 2020 02:04:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:72c2830c5e0823d3140db951e0d17bebf853e07105596b46555e00e1f02eb0da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68548448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd38dbb5fc575e2667c6c5e443b020b12a20e3e827a1284d8a8aa2c40a069a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

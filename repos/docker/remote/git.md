## `docker:git`

```console
$ docker pull docker@sha256:289b3feb29aab204757647a2910726d576765bb9e39b9a01810e3b439184e045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:09243d3a75d2835f75743bbe6b16c317f8f346c20b7d54d587fbc014d30b3483
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76220768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab537c792b4d7ba13194095c2000c76eb1d836e96fc996ccf2db889804cd98a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 16:14:46 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 23 Mar 2022 16:14:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 16:14:47 GMT
ENV DOCKER_VERSION=20.10.13
# Wed, 23 Mar 2022 16:14:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 23 Mar 2022 16:14:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 23 Mar 2022 16:14:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 23 Mar 2022 16:14:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 23 Mar 2022 16:14:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 23 Mar 2022 16:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 16:14:54 GMT
CMD ["sh"]
# Wed, 23 Mar 2022 16:15:13 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c236b952b9466b604bbc4e060a2667d7a7a335bee006fd5104c151dbdb4bf787`  
		Last Modified: Wed, 23 Mar 2022 16:15:39 GMT  
		Size: 2.0 MB (1969538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2580f7437ec44a9dd3670ee6fd964ecb068808106d1bd8b961e7a568ef3ceb4f`  
		Last Modified: Wed, 23 Mar 2022 16:15:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649ff060972a496aa084c1d3756524db829e6a242ae7bc9658bb9e16dba5eec`  
		Last Modified: Wed, 23 Mar 2022 16:15:47 GMT  
		Size: 64.6 MB (64612540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce146c1b1e3f178db76c3a214324f7973a9d400e00f4fe633915227312de816`  
		Last Modified: Wed, 23 Mar 2022 16:15:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e53e995f191e2dda8b29cb2d128726d68f640b669c634f9d7b7239cb49b0f2`  
		Last Modified: Wed, 23 Mar 2022 16:15:35 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf02f7e7ba89735873e4127a2b0d297b7bd256e05aa35b12310505f644e99e`  
		Last Modified: Wed, 23 Mar 2022 16:15:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1051b0ced9b69b0cf645b1f03d6ad5c392a111bc37db41841f0a03c28fcce3bf`  
		Last Modified: Wed, 23 Mar 2022 16:16:55 GMT  
		Size: 6.8 MB (6824140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:72b64e64f292fcc354064aff807584ba6aa24c62dcaacd0f4180974d732d7c33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70153837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a742244413c82313c84ffc8e2aae4a5e443443e2e7c6283b00bc9d89c10d767`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 06:44:43 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Thu, 17 Mar 2022 06:44:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 06:44:45 GMT
ENV DOCKER_VERSION=20.10.13
# Thu, 17 Mar 2022 06:44:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 17 Mar 2022 06:44:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 17 Mar 2022 06:44:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 17 Mar 2022 06:44:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 17 Mar 2022 06:44:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 17 Mar 2022 06:44:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 06:44:54 GMT
CMD ["sh"]
# Thu, 17 Mar 2022 06:45:36 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584bd6b2d67571b28ebbe22152f5536e3cff37d4346bc02a444b2ede9b5d71c6`  
		Last Modified: Thu, 17 Mar 2022 06:46:18 GMT  
		Size: 1.9 MB (1938905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadc398c63809a7b7b0d60cee36c1a95c7dd031fb5987cb99246b289df77d64f`  
		Last Modified: Thu, 17 Mar 2022 06:46:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fce163fc9e7e1d8912203364c303838e60da953ed77812572633504c2bd014`  
		Last Modified: Thu, 17 Mar 2022 06:46:25 GMT  
		Size: 58.6 MB (58565248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9a0a3a69cb84240c8270720f964d7155438567aa97bb868bfe1adc07b5b977`  
		Last Modified: Thu, 17 Mar 2022 06:46:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee8be56eb060db5cad28d2359c143a7a7de20610f090073f5cbd7f1cfeafbd4`  
		Last Modified: Thu, 17 Mar 2022 06:46:16 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746be13a2cb02a7014e32f66ba9fb3bb10e14bd43af45b7890fb09464fe2a830`  
		Last Modified: Thu, 17 Mar 2022 06:46:16 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716e163322a30318e4b5622ac98de0815fd95f93070ec60e4ee6ea3a3f85b59`  
		Last Modified: Thu, 17 Mar 2022 06:47:35 GMT  
		Size: 6.9 MB (6933048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

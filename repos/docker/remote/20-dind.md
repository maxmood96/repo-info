## `docker:20-dind`

```console
$ docker pull docker@sha256:fcbd7cae41740db4877d404a03c5807450dee8b82c38f9ba0aadebb9140a00d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:ec5878c9db35767e5ff292c496c07c67b0932c59596dc0e35816594edde1e87e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76136400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7345804dac56f89b033a4f69f7212a26e0f2588eb5d4ca570e02eff3f977a1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

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
# Wed, 23 Mar 2022 16:15:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 23 Mar 2022 16:15:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 23 Mar 2022 16:15:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 23 Mar 2022 16:15:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 23 Mar 2022 16:15:01 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 23 Mar 2022 16:15:01 GMT
VOLUME [/var/lib/docker]
# Wed, 23 Mar 2022 16:15:02 GMT
EXPOSE 2375 2376
# Wed, 23 Mar 2022 16:15:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 23 Mar 2022 16:15:02 GMT
CMD []
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
	-	`sha256:b410477bf81b8b92e3a28c6f882c9905a23f7e3838e49308c7f784ff3007d03e`  
		Last Modified: Wed, 23 Mar 2022 16:16:13 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e96caeccfc0826c39cd414081cf962b6a72675e2a3ca9de4c5d66ea494d6ed`  
		Last Modified: Wed, 23 Mar 2022 16:16:12 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfbb4c499a0c06e8d0bb1e960c5b670492826a111afccb95bd4743430e41a45`  
		Last Modified: Wed, 23 Mar 2022 16:16:12 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14191ab5ed939543bc615c16d372290873216683c9aa360998fa24ecaf7b970`  
		Last Modified: Wed, 23 Mar 2022 16:16:12 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e6222d4d8b30c439b883f691f52e8e405f6464852c86477f7b1577dee106ee6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69841345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ba71573c3cddc7fe6d1f68e3c7c55e13f7549be38cf07414563df801aa79e1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

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
# Thu, 17 Mar 2022 06:45:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 17 Mar 2022 06:45:07 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 17 Mar 2022 06:45:08 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 17 Mar 2022 06:45:09 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 17 Mar 2022 06:45:11 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 17 Mar 2022 06:45:11 GMT
VOLUME [/var/lib/docker]
# Thu, 17 Mar 2022 06:45:12 GMT
EXPOSE 2375 2376
# Thu, 17 Mar 2022 06:45:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 17 Mar 2022 06:45:14 GMT
CMD []
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
	-	`sha256:cb73bd4ce74defd0741f3f7922ffb261b2f91b45cf97e2225f65aaba2b4c42d6`  
		Last Modified: Thu, 17 Mar 2022 06:46:48 GMT  
		Size: 6.6 MB (6615563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e054635e9f383caa96af63cfbbc71098384c50f5c13efcc785d2a870ed8e4af9`  
		Last Modified: Thu, 17 Mar 2022 06:46:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791a50930d17375d4278a896defa85218b579b3efdd1455d1fa503e187676dfb`  
		Last Modified: Thu, 17 Mar 2022 06:46:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752ca04529521e0b4db8ded3d79d79f1629c7c725837b87fe79519f64bcb2e05`  
		Last Modified: Thu, 17 Mar 2022 06:46:47 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:ef4fb6a1255345d59ead278f6bf74be666e0e47cb075c237682bb266c0bfb3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:04fd1a7a19db9f3d0a9d95ef5ad79db235875a8a73af6850e6c5c22bc84cf862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74984029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646696d3b05ba82569ddaff6345806329dc6c177dd23e6827623b82b7ffd9e62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 12 Nov 2021 22:01:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 22:01:00 GMT
ENV DOCKER_VERSION=20.10.10
# Fri, 12 Nov 2021 22:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.10.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.10.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 12 Nov 2021 22:01:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 12 Nov 2021 22:01:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Nov 2021 22:01:12 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 12 Nov 2021 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:13 GMT
CMD ["sh"]
# Fri, 12 Nov 2021 22:01:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 12 Nov 2021 22:01:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:26 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 12 Nov 2021 22:01:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 12 Nov 2021 22:01:29 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:01:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Nov 2021 22:01:30 GMT
EXPOSE 2375 2376
# Fri, 12 Nov 2021 22:01:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Nov 2021 22:01:31 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b81e4bf1fdc42d15e4c1cfd4aa82e5fe027cf88bd858b5be7681ef621c617`  
		Last Modified: Fri, 12 Nov 2021 22:02:42 GMT  
		Size: 1.9 MB (1937203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da79b3d4ea6e72fe17974fcd737705b6da38e9063e5bbb26cea5a9fa7465bae`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9ed9eef89d1881a25c3f3e24fcfeaa7b25e9905ab6be33d81ca9de0d2c034`  
		Last Modified: Fri, 12 Nov 2021 22:02:54 GMT  
		Size: 63.7 MB (63694369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb21ac84428f3ef487a56b29d19f702b12f9832d0ff77c9d039c67b2d54384db`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b6d39fe806a6d72a91e74ce761746dbd95ea04c73bcf3adb6354a01e4bfd63`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3f5acafcc601ca43ce0ed797a9ad904e45951eb8b2478c71b5a25434d55b9c`  
		Last Modified: Fri, 12 Nov 2021 22:02:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0424728e541fc3dac6fe124afbbeafcdcaed60c2e02f1439f0e9c88a43b5b`  
		Last Modified: Fri, 12 Nov 2021 22:03:15 GMT  
		Size: 6.5 MB (6522724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3601851fa6560b0bd26d2cdf3c96ce399edf152a11db3403c61c1fcd874dd640`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aa4a947d580b2bc498eb5284f68f5de2738ab0f1e9d969752d69601f1376a5`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee5f376258a58aec71ed5db716acffcc095d38feceabe04b1907e80c4fdc86`  
		Last Modified: Fri, 12 Nov 2021 22:03:14 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6b91496cd8473f8f0412be846318dcf073a41e5c02fea27a75a657376c55e83b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68798719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9280bbaf2b20c01dbbcd50930cb5862adc44e531d88f54d157358d16f7de8a5f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:12:04 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 13 Nov 2021 11:12:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 18 Nov 2021 09:17:16 GMT
ENV DOCKER_VERSION=20.10.11
# Thu, 18 Nov 2021 09:17:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.11.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.11.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.11.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.11.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 18 Nov 2021 09:17:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 18 Nov 2021 09:17:25 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 18 Nov 2021 09:17:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Nov 2021 09:17:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 18 Nov 2021 09:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Nov 2021 09:17:28 GMT
CMD ["sh"]
# Thu, 18 Nov 2021 09:17:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 18 Nov 2021 09:17:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 18 Nov 2021 09:17:40 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 18 Nov 2021 09:17:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 18 Nov 2021 09:17:43 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Thu, 18 Nov 2021 09:17:43 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Nov 2021 09:17:44 GMT
EXPOSE 2375 2376
# Thu, 18 Nov 2021 09:17:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Nov 2021 09:17:46 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233f664f6e365c4259a38e7cfe3c14e234ab45f15847cc874a88b510f66a132f`  
		Last Modified: Sat, 13 Nov 2021 11:13:40 GMT  
		Size: 1.9 MB (1909969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501a1c7cbdd3e377ff292e68f9ced99315b84c85398591633343352948bbc291`  
		Last Modified: Sat, 13 Nov 2021 11:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50fed93df89351d596ab08fab482a174aa37a86d61cdeef150162665a67a80`  
		Last Modified: Thu, 18 Nov 2021 09:18:59 GMT  
		Size: 57.7 MB (57746015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21638a3c07c5ebd6977bcc9c75e0ac36c2a82b761fc51a8aee313c9a9d7ed46`  
		Last Modified: Thu, 18 Nov 2021 09:18:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e37a1bae185ca8552a00efd7984a74bc595d0dac82ab81e945615f5a0b29af`  
		Last Modified: Thu, 18 Nov 2021 09:18:49 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c4e38c2d1b6603791a26f4dad582d554c306fb4c8c4218e0d537da3b8af6a`  
		Last Modified: Thu, 18 Nov 2021 09:18:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc29a86f7ed1b15ec5c146abf64a41609779eb5b0e2a668d274b1b28c14c37e3`  
		Last Modified: Thu, 18 Nov 2021 09:19:20 GMT  
		Size: 6.4 MB (6418345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce285f2fd3dbcbe5e58749e817ef3a3e60fa1dbf82bc51eaff0f20f8e151d3f`  
		Last Modified: Thu, 18 Nov 2021 09:19:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabdc4aba67b4850e7e5c118e6409d59a161d11f5be536341a4e9f40ed017bf`  
		Last Modified: Thu, 18 Nov 2021 09:19:18 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd2d42122e3f199551259bf3db06d2c446c725eb3ae3239f2692f3fa57804b5`  
		Last Modified: Thu, 18 Nov 2021 09:19:18 GMT  
		Size: 2.6 KB (2614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

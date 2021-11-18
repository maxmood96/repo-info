## `docker:dind-rootless`

```console
$ docker pull docker@sha256:f7eda2fabb5f3b449e141975f3bd3b53a303f0976aeb06638626a6c49bfbc45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:edf71b73b3a20e77a4f8f69b37bc72582a114b278bd261d8648658d6c17cc857
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95259749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f3018944b3068b6ccad0cad95fe3712dcb72923cb2f4fcc11ac17e20c5f2b0`
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
# Fri, 12 Nov 2021 22:01:39 GMT
RUN apk add --no-cache iproute2
# Fri, 12 Nov 2021 22:01:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 12 Nov 2021 22:01:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 12 Nov 2021 22:01:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.10.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.10.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 12 Nov 2021 22:01:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 12 Nov 2021 22:01:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 12 Nov 2021 22:01:51 GMT
USER rootless
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
	-	`sha256:45e65c32f7feb2ca545e5be325979514421ae6452ffbb39555fc0ff558185ee8`  
		Last Modified: Fri, 12 Nov 2021 22:03:35 GMT  
		Size: 1.1 MB (1149132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791493f35b317dccba1da11b14d192d4a6ad0990ca703af9d9d8ef4e2bb27648`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b52cb220a5b157d4e3fb7e5810ede9299e89837bdbaa456fe479a7ef63e38b8`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf41e4bfb164e2b3470d582411b00c27cbd6fef248d65721f8e831e13a6ef569`  
		Last Modified: Fri, 12 Nov 2021 22:03:38 GMT  
		Size: 19.1 MB (19124871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b220a5803c6b5f3c60d16c70f281c7fda036290f7734521becd337abc10338d3`  
		Last Modified: Fri, 12 Nov 2021 22:03:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2441b89586372dc59c8fce28fc3fa0a6141193ad158d18482597187a7e1c9eeb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91070455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c509ba52a7374da993e6cf01a7147518857077192831cf839078772fa27881b`
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
# Thu, 18 Nov 2021 09:17:54 GMT
RUN apk add --no-cache iproute2
# Thu, 18 Nov 2021 09:17:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 18 Nov 2021 09:17:56 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 18 Nov 2021 09:17:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.11.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.11.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 18 Nov 2021 09:18:00 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 18 Nov 2021 09:18:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 18 Nov 2021 09:18:02 GMT
USER rootless
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
	-	`sha256:230963f6db0e75d3a58bc46d5b33ea4f67e6b1f0300e99ba12497c89f68ce855`  
		Last Modified: Thu, 18 Nov 2021 09:19:41 GMT  
		Size: 1.2 MB (1168585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66cc595973e50f8d3e25c628464cfa45436824aab478bda61c9ac4232d822c3`  
		Last Modified: Thu, 18 Nov 2021 09:19:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af54131c4a2bf83efebe4e4fec2d50bd4c99ffbca5aa5ccfa29c167f4c16ce`  
		Last Modified: Thu, 18 Nov 2021 09:19:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cab39e5c6b0a896c570c0218f29e0600936018957c487e7b439c9ecf14ad8e`  
		Last Modified: Thu, 18 Nov 2021 09:19:44 GMT  
		Size: 21.1 MB (21101528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b365691e2dffd5c75fa3b86bd4ccd1b11a4beae986f511ce5400a6a3d69b550c`  
		Last Modified: Thu, 18 Nov 2021 09:19:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

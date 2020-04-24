## `docker:dind`

```console
$ docker pull docker@sha256:09515aa8806183adcd89911c23ecbac74b713d89b4832a0f0551b460ea1c20a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:ecb51f5e1184ffe5c33dbb316b7ce13784807a8b209302ebb25b4ffbf4c51e1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74577823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7799c84f00cd5b6d6c537ef3e0211866e35f09cfcfca6f979c9df1098e55b365`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:13:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 14:13:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:13:45 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 14:13:46 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 14:13:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 14:13:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 14:13:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 14:13:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 14:13:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 14:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 14:13:54 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 14:13:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 14:14:00 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 14:14:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 14:14:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 24 Apr 2020 14:14:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Fri, 24 Apr 2020 14:14:02 GMT
VOLUME [/var/lib/docker]
# Fri, 24 Apr 2020 14:14:02 GMT
EXPOSE 2375 2376
# Fri, 24 Apr 2020 14:14:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 24 Apr 2020 14:14:02 GMT
CMD []
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c731d6eb3df3a5c5587aacd253a9f6d985fafb5a1c8ea03add752b00888ec`  
		Last Modified: Fri, 24 Apr 2020 14:14:46 GMT  
		Size: 2.0 MB (1994349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79d4ac3cd039c6e3f17d157c79b369e68a1a0d79c310a699cfd4835e283d48`  
		Last Modified: Fri, 24 Apr 2020 14:14:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65de10866d6a6dedf15a6639d25cd751c00bc00686d105b1b421196eb9c064be`  
		Last Modified: Fri, 24 Apr 2020 14:14:59 GMT  
		Size: 64.2 MB (64218864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd69ed7f17f1afd8fc89390cff7c918080008fa3cded268071c413e8ea85bd0`  
		Last Modified: Fri, 24 Apr 2020 14:14:44 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ba9e5a2fa609630ccb69342d386a4315fe5eaf4784859867053d847ca1d0dc`  
		Last Modified: Fri, 24 Apr 2020 14:14:44 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75478c283dd28cb16ded5ff60c6b8e81006d4c0b79ec289a425a333d9831b88c`  
		Last Modified: Fri, 24 Apr 2020 14:14:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a34b06546beeca35ff6aeeb620ae529071cca7e4bd7b346d4435c13f8279f9d`  
		Last Modified: Fri, 24 Apr 2020 14:15:07 GMT  
		Size: 5.5 MB (5544892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf9fe696821b8ea7376463193e3721b376466b86970a07c6b99938c210fd63b`  
		Last Modified: Fri, 24 Apr 2020 14:15:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326857604f3383aaef75d4929bb5f1cf4f09a56611a5ce3508c1962a5b33cb7f`  
		Last Modified: Fri, 24 Apr 2020 14:15:06 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8949ad47c3a99ddbefb7d70e58a55d1138524c5250c7a60c1fa33cfa73d5382a`  
		Last Modified: Fri, 24 Apr 2020 14:15:06 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a915b41907ccdac67873987fa8f7c4f45aa7267445252e0487837bc04890f0c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b46d62e3b3303c9c8197d152969777185471b313ebb9fad5dd801aefc71883`
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
# Thu, 23 Apr 2020 17:13:30 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:13:31 GMT
VOLUME [/var/lib/docker]
# Thu, 23 Apr 2020 17:13:32 GMT
EXPOSE 2375 2376
# Thu, 23 Apr 2020 17:13:34 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 23 Apr 2020 17:13:35 GMT
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
	-	`sha256:b0941cd493b1305cefbed72fc7a954510a252aecf9cf88b6f68597051024c492`  
		Last Modified: Thu, 23 Apr 2020 17:14:37 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c965d2533dd8e15540b8e9eaed5924ad3c85467cf8ef5f15a383e4c49e4989f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67003127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52649ba615f63d2aee9c20dddedf1bac1a3287900af84ae79c449cab8617ed59`
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
# Fri, 24 Apr 2020 02:04:21 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Fri, 24 Apr 2020 02:04:22 GMT
VOLUME [/var/lib/docker]
# Fri, 24 Apr 2020 02:04:23 GMT
EXPOSE 2375 2376
# Fri, 24 Apr 2020 02:04:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 24 Apr 2020 02:04:25 GMT
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
	-	`sha256:40601317ba946c8ad0de541d7211f4d241876d4e77f424e786b9fa655cd396e4`  
		Last Modified: Fri, 24 Apr 2020 02:05:28 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d2998b7f4f1f5d55fdb669b3fa32165ca1abfd479c788d478a70113e51bfaf28
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004774411bb2850757dafb1b670b32ca64805946e12b721ad9e7661d28f037be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:18:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 09:18:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 09:18:55 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 24 Apr 2020 09:18:56 GMT
ENV DOCKER_VERSION=19.03.8
# Fri, 24 Apr 2020 09:19:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 24 Apr 2020 09:19:05 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 24 Apr 2020 09:19:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:19:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 24 Apr 2020 09:19:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 24 Apr 2020 09:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:19:13 GMT
CMD ["sh"]
# Fri, 24 Apr 2020 09:19:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 24 Apr 2020 09:19:30 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 24 Apr 2020 09:19:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 24 Apr 2020 09:19:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 24 Apr 2020 09:19:34 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:19:34 GMT
VOLUME [/var/lib/docker]
# Fri, 24 Apr 2020 09:19:35 GMT
EXPOSE 2375 2376
# Fri, 24 Apr 2020 09:19:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 24 Apr 2020 09:19:36 GMT
CMD []
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be38edc41e1b9f030768c829de52d1a1689186ab80285cc4c7bbf947d610828`  
		Last Modified: Fri, 24 Apr 2020 09:20:06 GMT  
		Size: 2.0 MB (2014043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3afb04d5997d58b56418c9930b6d02c288ea479ec452e45a04492177194079`  
		Last Modified: Fri, 24 Apr 2020 09:20:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b74c254a8ac3029945c55c615aebf2f91a8464887ba6df5ad81584524980d3`  
		Last Modified: Fri, 24 Apr 2020 09:20:21 GMT  
		Size: 57.4 MB (57387281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee44a9dabb3da6e61f9dbad6dd43e381a3bc7b7b8520ec4664edc582d02e9f`  
		Last Modified: Fri, 24 Apr 2020 09:20:03 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d1ef7be7cf7149e70f06fe1a0c965629e635abd4e43ebba681da227cea275`  
		Last Modified: Fri, 24 Apr 2020 09:20:03 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8486642a619f43cacb15684b4905c7f1792ed755ca757c0cb8685b2fbee29f5a`  
		Last Modified: Fri, 24 Apr 2020 09:20:03 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307f8efc9d1feaf2dff893510778c57dbea0b87b22f72b6b93c2122a3cd77e14`  
		Last Modified: Fri, 24 Apr 2020 09:20:43 GMT  
		Size: 5.5 MB (5545625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d81b4e1f1baf5e9eee18f6db5553b2eb230aa46872d3bfba2c253c6cbb489f`  
		Last Modified: Fri, 24 Apr 2020 09:20:42 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4589fcc7577ce2f186d99ebcd30f471868c21a2ae207e8bd8343763c06fde76e`  
		Last Modified: Fri, 24 Apr 2020 09:20:42 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736ee4717f3625d5bd4e9ee30be88a6979d434b8cb3ae0a70daaa5733d6aa1c5`  
		Last Modified: Fri, 24 Apr 2020 09:20:42 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:d5d327d4e5085de37787d0fd1647c5291f0644749467f3c9e9197316acc412df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:c9fe80d9eb030d771811e9cefcf2e3cb73aad845c24eee8e29b72b4429fae283
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66536142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51453dcdd9bd51e503f75e6d42a4071469ad2ba816321781985041b6bc7776db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 04 Aug 2021 21:20:35 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 04 Aug 2021 21:20:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 04 Aug 2021 21:20:36 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 04 Aug 2021 21:20:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 04 Aug 2021 21:20:43 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 04 Aug 2021 21:20:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 04 Aug 2021 21:20:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Aug 2021 21:20:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 04 Aug 2021 21:20:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Aug 2021 21:20:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b94fafbd542a8c279f4a08e81fef317862b0fe3f604febe2fc2138886ba1d7`  
		Last Modified: Wed, 04 Aug 2021 21:21:53 GMT  
		Size: 2.4 MB (2438245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e3c9e6c132861fd24ac22906718bb610ebcf3912ade5e48a791ba8f85e5799`  
		Last Modified: Wed, 04 Aug 2021 21:21:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc990f87bf12a7b8fb86c3003977468a14fb1a31e5bb0b500e8127ee4e6beb5`  
		Last Modified: Wed, 04 Aug 2021 21:22:03 GMT  
		Size: 61.3 MB (61284061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1436504743cc47a166b7964d591792b69e34aa1e3e07ef5d91f481fdb11f948d`  
		Last Modified: Wed, 04 Aug 2021 21:21:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c526f01240b836e9645a2b2b629051c5e488d60b309d5f253adab7f2c45ed7`  
		Last Modified: Wed, 04 Aug 2021 21:21:50 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d263b0ed3ea3116c812ca5c542c5175ccb0c99bee76b06db8c2340290057fa`  
		Last Modified: Wed, 04 Aug 2021 21:21:51 GMT  
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
$ docker pull docker@sha256:202f4fd8f1bc62e516f42f1f32d205a6d9dc12a5eddf42be5adda612331f7d99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60592580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917aa76b39804498915883c81d9c3f4616dafbae602e0e81597852ab6905bc77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Aug 2021 21:40:35 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 04 Aug 2021 21:40:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 04 Aug 2021 21:40:35 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 04 Aug 2021 21:40:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 04 Aug 2021 21:40:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 04 Aug 2021 21:40:39 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 04 Aug 2021 21:40:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Aug 2021 21:40:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 04 Aug 2021 21:40:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Aug 2021 21:40:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d668eead8965ee8f4a1cd65de2a1cde9c49cfd2c2f06ac2290e0b90724ba4ea3`  
		Last Modified: Wed, 04 Aug 2021 21:42:32 GMT  
		Size: 2.5 MB (2458333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7010a04da6233aa993b677900fe12554cb30e4b12adeee36a2c884d5c0ec8965`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c06e26407aeefb6fd4953cb12e19c70695281c4c9ab4e9b8120734669094a8a`  
		Last Modified: Wed, 04 Aug 2021 21:42:39 GMT  
		Size: 55.4 MB (55420354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674e4b73ac390f4f52af96ffa7e98228c80619fa25bd61e862485f64b509a849`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627ac7844e75fc94ea8963915c871cb5e376af3631da0ce14bf5a5662813175f`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be33fcd733ebf68f8983483238e2245237efdc7751c83d98e9ce9b6a0f3069f`  
		Last Modified: Wed, 04 Aug 2021 21:42:29 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

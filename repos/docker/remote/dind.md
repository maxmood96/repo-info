## `docker:dind`

```console
$ docker pull docker@sha256:a4f33d003b7ec9133c2a1ff61f4e80305b329c0fa8b753140b9ab2808f28328c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:c260a7abfc7f5f8c20eb3918d5fce58c17018d6d9490ce1b3a950d9aa9e404ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74997968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33335bfe8302f4d8a7688bc1fa539f2aba787ec724119be53adc4681702a3e7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 14 Feb 2020 01:19:29 GMT
ENV DOCKER_VERSION=19.03.6
# Fri, 14 Feb 2020 01:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 14 Feb 2020 01:19:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 14 Feb 2020 01:19:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 14 Feb 2020 01:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Feb 2020 01:19:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 14 Feb 2020 01:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2020 01:19:36 GMT
CMD ["sh"]
# Fri, 14 Feb 2020 01:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 14 Feb 2020 01:19:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 14 Feb 2020 01:19:43 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 14 Feb 2020 01:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 14 Feb 2020 01:19:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 14 Feb 2020 01:19:44 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Feb 2020 01:19:44 GMT
EXPOSE 2375 2376
# Fri, 14 Feb 2020 01:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Feb 2020 01:19:45 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a3718af66353ac1b9b61d460169dacea8af2b828fc5a4c145ada71853c1004`  
		Last Modified: Fri, 14 Feb 2020 01:20:39 GMT  
		Size: 64.2 MB (64176130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d685e7204c1caa1e6279ffe73ab17529d60ea1692d2ce9e5bcd82607e72b34`  
		Last Modified: Fri, 14 Feb 2020 01:20:25 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2db148201ed411ce26f0d6f48b5b112ce88292c9ef4bccff01da8443e19e29`  
		Last Modified: Fri, 14 Feb 2020 01:20:25 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419c00a7b0350cd0fdcab8d5856822508e0f6ceefc5220342dabb3aabc23ccaf`  
		Last Modified: Fri, 14 Feb 2020 01:20:25 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cb82cf49416af7d1de7ebe13f3325245f28edd1649b3ae3d845db5b79e1b54`  
		Last Modified: Fri, 14 Feb 2020 01:20:47 GMT  
		Size: 5.6 MB (5587326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db666592efe5d25d406b538d41a46547bc1ee51698fcea3fc61fb9d79ac1b4be`  
		Last Modified: Fri, 14 Feb 2020 01:20:46 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c2ab5c34a68d6bcd5e582c67f7050475fb4964608cfd31f5b7b56889db1019`  
		Last Modified: Fri, 14 Feb 2020 01:20:46 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ab1e2460ab171c3b002e555f427232ba07879374ca4db150cf5a90bbb64c84`  
		Last Modified: Fri, 14 Feb 2020 01:20:46 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0dfb71acca3429f640bbadf8624943f282c865647ad5b196d72c6a2975649ef5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68097457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34716af654fcc0f8e63f802d9b8cc20fbed7e913c7f3d79034468738ee01972a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 14 Feb 2020 00:49:26 GMT
ENV DOCKER_VERSION=19.03.6
# Fri, 14 Feb 2020 00:49:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 14 Feb 2020 00:49:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 14 Feb 2020 00:49:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 14 Feb 2020 00:49:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Feb 2020 00:49:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 14 Feb 2020 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2020 00:49:51 GMT
CMD ["sh"]
# Fri, 14 Feb 2020 00:50:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 14 Feb 2020 00:50:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 14 Feb 2020 00:50:09 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 14 Feb 2020 00:50:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 14 Feb 2020 00:50:12 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 14 Feb 2020 00:50:13 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Feb 2020 00:50:14 GMT
EXPOSE 2375 2376
# Fri, 14 Feb 2020 00:50:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Feb 2020 00:50:16 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ab93f21a8d6772b88c5f08c9e9eb991b35f4c1af9eff01e7364d6807e06bb1`  
		Last Modified: Fri, 14 Feb 2020 00:51:09 GMT  
		Size: 59.9 MB (59902626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a911b2eeb709ad1c00a244250662b3fd574f25b9ab69126c5dcdc9bb7c216616`  
		Last Modified: Fri, 14 Feb 2020 00:50:43 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c4f60c2d818ce89405acbbe5e22d642eef555b74e86c6635efb34149190ab`  
		Last Modified: Fri, 14 Feb 2020 00:50:43 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4854298ccec6a9b2e6638aea573816cdf8c9f7be598f33d18bdf42763e6cf2`  
		Last Modified: Fri, 14 Feb 2020 00:50:43 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b580a6cce9b14a37b83c24329f511f76ee1ac87468f6cb8ef749ee87b8357179`  
		Last Modified: Fri, 14 Feb 2020 00:51:22 GMT  
		Size: 3.2 MB (3215399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221853bc422bef424dc5a8d3ef2adc6917b7eb8e9069923ac87e5066176acd9c`  
		Last Modified: Fri, 14 Feb 2020 00:51:22 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585e62a11a914b232060befdd11c055120bc0210c0deb7a921a85554696a6d97`  
		Last Modified: Fri, 14 Feb 2020 00:51:22 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b8aa2e9b4c813fa8323cab041b917ff56c71db6c211a53e32cf6f71d8d823`  
		Last Modified: Fri, 14 Feb 2020 00:51:22 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5aa24a7e4e5ab077aea41336c9a396cedf6daa0f745455e6e5aabc741254f5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67451838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca3ed1a1a682b830fe40c62f4cf9a73839f4ef1925b2bfb9b43a4435d07d311`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 14 Feb 2020 00:57:29 GMT
ENV DOCKER_VERSION=19.03.6
# Fri, 14 Feb 2020 00:57:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 14 Feb 2020 00:57:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 14 Feb 2020 00:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 14 Feb 2020 00:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Feb 2020 00:57:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 14 Feb 2020 00:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2020 00:57:51 GMT
CMD ["sh"]
# Fri, 14 Feb 2020 00:58:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 14 Feb 2020 00:58:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 14 Feb 2020 00:58:09 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 14 Feb 2020 00:58:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 14 Feb 2020 00:58:13 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 14 Feb 2020 00:58:14 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Feb 2020 00:58:16 GMT
EXPOSE 2375 2376
# Fri, 14 Feb 2020 00:58:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Feb 2020 00:58:18 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b5851c6f15fe6a2c1d6e6331a0e51663353c32ae2e933dcc2f7991e6d6c03`  
		Last Modified: Fri, 14 Feb 2020 00:59:13 GMT  
		Size: 59.9 MB (59892891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20c8b17450265615f7f65f01fb90bf1bacf011a127e2f9fda78b06c77a70fab`  
		Last Modified: Fri, 14 Feb 2020 00:58:52 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97228220539ded6a04a9317e0319ef5472e15fd7df409964b26ff46ee4aa1992`  
		Last Modified: Fri, 14 Feb 2020 00:58:52 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20888b928fe0e2e08fd76122cc22ec6950031292b58aed2886f5eea8f0527d1c`  
		Last Modified: Fri, 14 Feb 2020 00:58:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd757b082c4b2f7fbb7e61725aca14d5b89e70e1acbb41bc19ce68374bbc11c6`  
		Last Modified: Fri, 14 Feb 2020 00:59:25 GMT  
		Size: 2.9 MB (2878531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b405a8be391851f1884c27c0a30e9895b043c0bd7a29ac74c84e76b2b0a1655b`  
		Last Modified: Fri, 14 Feb 2020 00:59:24 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfec49d769bb63f056dbdcc81bfd5cbeacf33a45b73c0c0dac7049760b611ca`  
		Last Modified: Fri, 14 Feb 2020 00:59:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d7d95bf4b37f04c3d660d36ae57882355a6c1a991c7da654e39154037d019`  
		Last Modified: Fri, 14 Feb 2020 00:59:24 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:43bf267f694b75495a9a9b4292d158d72247209940842e097604fb2007630c9e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68111391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0711bd1e504586ae2857a5f87e210bd0b53e377d398a99694796e76cc5f01be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 14 Feb 2020 00:40:12 GMT
ENV DOCKER_VERSION=19.03.6
# Fri, 14 Feb 2020 00:40:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 14 Feb 2020 00:40:20 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 14 Feb 2020 00:40:21 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 14 Feb 2020 00:40:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Feb 2020 00:40:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 14 Feb 2020 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2020 00:40:25 GMT
CMD ["sh"]
# Fri, 14 Feb 2020 00:40:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 14 Feb 2020 00:40:36 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 14 Feb 2020 00:40:36 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 14 Feb 2020 00:40:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 14 Feb 2020 00:40:39 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 14 Feb 2020 00:40:40 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Feb 2020 00:40:42 GMT
EXPOSE 2375 2376
# Fri, 14 Feb 2020 00:40:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Feb 2020 00:40:45 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91ed599925cffa714c21263f87738f415991ddca6989e83b1338fb36f27b4d9`  
		Last Modified: Fri, 14 Feb 2020 00:41:29 GMT  
		Size: 57.3 MB (57346937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f904540acaf25838fd2d6aa92903dffff68d02ae287a79e63439360c25cce1`  
		Last Modified: Fri, 14 Feb 2020 00:41:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b692ba2de145eb720b9325fd54012571a4b27fce56a9730753a0fea4ea84727a`  
		Last Modified: Fri, 14 Feb 2020 00:41:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20adc8023b7adc8d8a0e7694239e7f296ffc86782d7e0a9e8a5e9e1fa97ade7`  
		Last Modified: Fri, 14 Feb 2020 00:41:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0508e36636ed1a6bdc5d46e44ab6dc559f18ceec9d96570cf6ff01a8017a5418`  
		Last Modified: Fri, 14 Feb 2020 00:41:41 GMT  
		Size: 5.6 MB (5589199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc8217f7911c0cd6e9b937c9c829e19993557dcde0fd6b20467ac3875887772`  
		Last Modified: Fri, 14 Feb 2020 00:41:40 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1de4f23f806fe2e2bb65db398fb5faaa8dabe4918ec95e506f391ce3e837b2`  
		Last Modified: Fri, 14 Feb 2020 00:41:40 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de4106ffe3b9d22b6cbe3b7412578695c4e435b481423c76b103730d52cc7b1`  
		Last Modified: Fri, 14 Feb 2020 00:41:40 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

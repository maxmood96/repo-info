## `docker:rc-dind`

```console
$ docker pull docker@sha256:7f81bbb44543583be6408b63dc1ddd53bb4f288cf630afbb27efc7957477186e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:5dcae0ac57467e2a655a9db6a1fea6c53a77c7621639e025a5bbe02fd24aba33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74648403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10251e5bf5394bb42f19475a0a6803ee437a05749217e7d38531652b6c485628`
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
# Wed, 29 Jan 2020 19:20:00 GMT
ENV DOCKER_CHANNEL=test
# Wed, 29 Jan 2020 19:20:00 GMT
ENV DOCKER_VERSION=19.03.6-rc1
# Wed, 29 Jan 2020 19:20:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 29 Jan 2020 19:20:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 29 Jan 2020 19:20:06 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:20:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 29 Jan 2020 19:20:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 29 Jan 2020 19:20:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2020 19:20:07 GMT
CMD ["sh"]
# Wed, 29 Jan 2020 19:20:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 29 Jan 2020 19:20:14 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:20:14 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 29 Jan 2020 19:20:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 29 Jan 2020 19:20:15 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:20:15 GMT
VOLUME [/var/lib/docker]
# Wed, 29 Jan 2020 19:20:16 GMT
EXPOSE 2375 2376
# Wed, 29 Jan 2020 19:20:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 29 Jan 2020 19:20:16 GMT
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
	-	`sha256:358e21eda998eac8678b36f6760ec1c4e78660dde5aa28ac38c98467e5e9066e`  
		Last Modified: Wed, 29 Jan 2020 19:21:30 GMT  
		Size: 63.8 MB (63826549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b55c1f6c3948d610e8583d86c32c17b57f98f83492b8a24d5c55634b9ed55`  
		Last Modified: Wed, 29 Jan 2020 19:21:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e507231c90c36c09ef35a10198d3d47fece99562d7b341b341427e5dac728c7`  
		Last Modified: Wed, 29 Jan 2020 19:21:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811a444a54828869cddc5006db913db387b8dcc4b783f5f5954ef9f39742ebe7`  
		Last Modified: Wed, 29 Jan 2020 19:21:17 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7499ee408427a75015f89d5ef4caf017fa155f9086f65d72beea8224e020a6c`  
		Last Modified: Wed, 29 Jan 2020 19:21:37 GMT  
		Size: 5.6 MB (5587345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3726f7345c731df08e212b54418fbb1ecffa53013791a7a64f986b5c83a79c`  
		Last Modified: Wed, 29 Jan 2020 19:21:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cb3aa874c2d9362d6fbea3e11f5839b14cac09980d0f262610f327e04ce2b9`  
		Last Modified: Wed, 29 Jan 2020 19:21:36 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f981c353abeb22f242120466b1f6de51a1e384b8458f1d70588eb21d3271782`  
		Last Modified: Wed, 29 Jan 2020 19:21:35 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:94164e68ab919ada666ca2e6521a3515eff362ce5cfa5bb5b95be58019feda51
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67758382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa6b481a695c3b3fb98552b6c6618fc9bcafb2c8dade9434aa623c49b0c6cd9`
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
# Wed, 29 Jan 2020 19:49:55 GMT
ENV DOCKER_CHANNEL=test
# Wed, 29 Jan 2020 19:49:56 GMT
ENV DOCKER_VERSION=19.03.6-rc1
# Wed, 29 Jan 2020 19:50:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 29 Jan 2020 19:50:10 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 29 Jan 2020 19:50:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:50:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 29 Jan 2020 19:50:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 29 Jan 2020 19:50:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2020 19:50:15 GMT
CMD ["sh"]
# Wed, 29 Jan 2020 19:50:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 29 Jan 2020 19:50:28 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:50:29 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 29 Jan 2020 19:50:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 29 Jan 2020 19:50:33 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:50:34 GMT
VOLUME [/var/lib/docker]
# Wed, 29 Jan 2020 19:50:36 GMT
EXPOSE 2375 2376
# Wed, 29 Jan 2020 19:50:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 29 Jan 2020 19:50:38 GMT
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
	-	`sha256:acdd8eb549c3043d120d4836ea740cb913ed05037d0d26a4ca7c9f6c8d2ccb7e`  
		Last Modified: Wed, 29 Jan 2020 19:51:53 GMT  
		Size: 59.6 MB (59563545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c134be06928945269fba0308cc7360de76e9d5b10922ac48f3c94370907cbe`  
		Last Modified: Wed, 29 Jan 2020 19:51:26 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793b58c2c66a180161dd2614d8e8c34971f2768635ac1166d9413fed2b90e65`  
		Last Modified: Wed, 29 Jan 2020 19:51:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8dacde58d6c1c1662466dd29007b4d9790b22cfebdd41c624e4f4043e948c6`  
		Last Modified: Wed, 29 Jan 2020 19:51:26 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ae7990939744eb9fd2629f5275e4903cb2f0895a43beb647eeb5d6943453b5`  
		Last Modified: Wed, 29 Jan 2020 19:52:04 GMT  
		Size: 3.2 MB (3215410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d827430f9884d08f37111c166758f67bfa07282fe8ff4c1cb3658cf506d6a95`  
		Last Modified: Wed, 29 Jan 2020 19:52:02 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0307a8f7718f1f865f4e069d9651d0a0bc4cba98c286a54ceff63633f62d3dc`  
		Last Modified: Wed, 29 Jan 2020 19:52:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3841568b239bef093b8e174d6f4924b86ee3f19ef38f91683a20f76c1d1335`  
		Last Modified: Wed, 29 Jan 2020 19:52:03 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:8fff95c1347479f67f09db6c87913c88a2004fa32be6026e19a2fdbe671459b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67108673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7741d5ff4cfe63ed91551f3c4fe1272da437d4dfbe086eca1e218086ba028f9e`
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
# Wed, 29 Jan 2020 19:57:32 GMT
ENV DOCKER_CHANNEL=test
# Wed, 29 Jan 2020 19:57:33 GMT
ENV DOCKER_VERSION=19.03.6-rc1
# Wed, 29 Jan 2020 19:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 29 Jan 2020 19:57:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 29 Jan 2020 19:57:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:57:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 29 Jan 2020 19:57:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 29 Jan 2020 19:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2020 19:57:52 GMT
CMD ["sh"]
# Wed, 29 Jan 2020 19:58:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 29 Jan 2020 19:58:04 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:58:05 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 29 Jan 2020 19:58:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 29 Jan 2020 19:58:08 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:58:08 GMT
VOLUME [/var/lib/docker]
# Wed, 29 Jan 2020 19:58:09 GMT
EXPOSE 2375 2376
# Wed, 29 Jan 2020 19:58:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 29 Jan 2020 19:58:10 GMT
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
	-	`sha256:2376c57585fa7285c8945f2745c4761039c09f197742bf05b7aa6aec9a981728`  
		Last Modified: Wed, 29 Jan 2020 19:59:19 GMT  
		Size: 59.5 MB (59549712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceb868d4f8058db091f450df0260fe4e317614c6622ee35108e8fa259847b8e`  
		Last Modified: Wed, 29 Jan 2020 19:58:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a9362f63035a6f83f5fe6a0dd8445f1761e0780e2ad65163dec58325acc663`  
		Last Modified: Wed, 29 Jan 2020 19:58:57 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a62c58bcf641dc34f639bfb165b4b5bbb8148e6c17bc2e59a2ca77804c82adf`  
		Last Modified: Wed, 29 Jan 2020 19:58:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89411248e146aa97930698a5b606144c51fa3d5f7b2dc1f57c36d292aecc59e`  
		Last Modified: Wed, 29 Jan 2020 19:59:37 GMT  
		Size: 2.9 MB (2878548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f47f10f2a403a743afe392deed7163019c4cce2d8c60758b533b2679203a6f`  
		Last Modified: Wed, 29 Jan 2020 19:59:36 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88be7550408f0fa67613fc8e9c5ddb3dcd8473850597b40a4353b9028521c85`  
		Last Modified: Wed, 29 Jan 2020 19:59:36 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93436f3b8bcd6799b32e5d837c34e551f76cdea17217706c20c0ee0e360daa13`  
		Last Modified: Wed, 29 Jan 2020 19:59:36 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4759108a005d44ade8c0b220e9537b8e80c6ff7cbe0db6a602619af5d351ad18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67793190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b608208fd33e56ad90233372606dedb9f4d1efc45f5e8aa4241af9a62706a2b`
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
# Wed, 29 Jan 2020 19:39:53 GMT
ENV DOCKER_CHANNEL=test
# Wed, 29 Jan 2020 19:39:54 GMT
ENV DOCKER_VERSION=19.03.6-rc1
# Wed, 29 Jan 2020 19:40:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 29 Jan 2020 19:40:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 29 Jan 2020 19:40:02 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:40:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 29 Jan 2020 19:40:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 29 Jan 2020 19:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2020 19:40:05 GMT
CMD ["sh"]
# Wed, 29 Jan 2020 19:40:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 29 Jan 2020 19:40:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:40:19 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 29 Jan 2020 19:40:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 29 Jan 2020 19:40:21 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Wed, 29 Jan 2020 19:40:22 GMT
VOLUME [/var/lib/docker]
# Wed, 29 Jan 2020 19:40:23 GMT
EXPOSE 2375 2376
# Wed, 29 Jan 2020 19:40:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 29 Jan 2020 19:40:24 GMT
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
	-	`sha256:c8a6ec73b6bfcc8b9f31ad36498039fbbb4b0a830bc9606a392f752439e10ad9`  
		Last Modified: Wed, 29 Jan 2020 19:41:28 GMT  
		Size: 57.0 MB (57028568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2344ba53d4a55121ad2c0aef4d0cd39ef0ed49778885604d2ec2b9220254827`  
		Last Modified: Wed, 29 Jan 2020 19:41:08 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a5d2f295d60c05fb92c8f1ce307a8d3c85af55dbdc2abbec8a43688d8e0656`  
		Last Modified: Wed, 29 Jan 2020 19:41:08 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26aa8ab1e30630143c3410d6027c9b29c6f4e243b8dc6490b872a4e1febf1a1`  
		Last Modified: Wed, 29 Jan 2020 19:41:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477b10f4f519c4e41b7ddb64d6ccd5622b488b4121dd53b657f52ffbaa74a4c`  
		Last Modified: Wed, 29 Jan 2020 19:41:38 GMT  
		Size: 5.6 MB (5589372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7627521aea433dcb0d1b7bd7e9a6aeabd06f0a4e59980f0383b2b9fef8a9a118`  
		Last Modified: Wed, 29 Jan 2020 19:41:37 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8f9f45550324f8da4a98211440febbaf96e2f9b67f3db52fa0510ce96b5ae3`  
		Last Modified: Wed, 29 Jan 2020 19:41:36 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed90d385abb5c469f2c8a8abf7c0a011dfcbc70c99b794080074ef3ab410b79`  
		Last Modified: Wed, 29 Jan 2020 19:41:36 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

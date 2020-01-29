<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:19`](#docker19)
-	[`docker:19.03`](#docker1903)
-	[`docker:19.03.5`](#docker19035)
-	[`docker:19.03.5-dind`](#docker19035-dind)
-	[`docker:19.03.5-dind-rootless`](#docker19035-dind-rootless)
-	[`docker:19.03.5-git`](#docker19035-git)
-	[`docker:19.03.6-rc1`](#docker19036-rc1)
-	[`docker:19.03.6-rc1-dind`](#docker19036-rc1-dind)
-	[`docker:19.03.6-rc1-dind-rootless`](#docker19036-rc1-dind-rootless)
-	[`docker:19.03.6-rc1-git`](#docker19036-rc1-git)
-	[`docker:19.03-dind`](#docker1903-dind)
-	[`docker:19.03-dind-rootless`](#docker1903-dind-rootless)
-	[`docker:19.03-git`](#docker1903-git)
-	[`docker:19.03-rc`](#docker1903-rc)
-	[`docker:19.03-rc-dind`](#docker1903-rc-dind)
-	[`docker:19.03-rc-dind-rootless`](#docker1903-rc-dind-rootless)
-	[`docker:19.03-rc-git`](#docker1903-rc-git)
-	[`docker:19-dind`](#docker19-dind)
-	[`docker:19-dind-rootless`](#docker19-dind-rootless)
-	[`docker:19-git`](#docker19-git)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:rc`](#dockerrc)
-	[`docker:rc-dind`](#dockerrc-dind)
-	[`docker:rc-dind-rootless`](#dockerrc-dind-rootless)
-	[`docker:rc-git`](#dockerrc-git)
-	[`docker:stable`](#dockerstable)
-	[`docker:stable-dind`](#dockerstable-dind)
-	[`docker:stable-dind-rootless`](#dockerstable-dind-rootless)
-	[`docker:stable-git`](#dockerstable-git)
-	[`docker:test`](#dockertest)
-	[`docker:test-dind`](#dockertest-dind)
-	[`docker:test-dind-rootless`](#dockertest-dind-rootless)
-	[`docker:test-git`](#dockertest-git)

## `docker:19`

```console
$ docker pull docker@sha256:0b90b0aefd15794e4d5bea2debc3b761c1d3481a92ec7166f8453652d0deba95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19` - linux; amd64

```console
$ docker pull docker@sha256:48db0e29e2214d564b66daffc707ad290c8788dc655cea59c605f021790d38a0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69033024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c774f62a9b520060d72c3c1901facdfdfd0fc4ae7c5e817cdaf6acd456432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v6

```console
$ docker pull docker@sha256:aa908727daa7433a0d156f6c6703fe5d945c4019e8b7f5d0c4fc8213e6d67fed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64511941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e68c26581b5f619c73bdd54951308df6920447f7be745bea2bfbb6b3624b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v7

```console
$ docker pull docker@sha256:ec6f3f2f65803962bd623ab2de639bd87d41d856c6ef477ae58383b379a1376a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fc3364d97bc6d5e8c8de60fa7c776bbc4eb6ca32c38029201f27c506086b11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e09d98b19bbee9f15b9f66604d48401833716faef061e9e509b48fb8db8bd1c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466581031774ac8ddb27699e61f2fbf858fce357adad7352cc410ef9ad6344bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03`

```console
$ docker pull docker@sha256:0b90b0aefd15794e4d5bea2debc3b761c1d3481a92ec7166f8453652d0deba95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03` - linux; amd64

```console
$ docker pull docker@sha256:48db0e29e2214d564b66daffc707ad290c8788dc655cea59c605f021790d38a0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69033024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c774f62a9b520060d72c3c1901facdfdfd0fc4ae7c5e817cdaf6acd456432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v6

```console
$ docker pull docker@sha256:aa908727daa7433a0d156f6c6703fe5d945c4019e8b7f5d0c4fc8213e6d67fed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64511941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e68c26581b5f619c73bdd54951308df6920447f7be745bea2bfbb6b3624b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v7

```console
$ docker pull docker@sha256:ec6f3f2f65803962bd623ab2de639bd87d41d856c6ef477ae58383b379a1376a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fc3364d97bc6d5e8c8de60fa7c776bbc4eb6ca32c38029201f27c506086b11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e09d98b19bbee9f15b9f66604d48401833716faef061e9e509b48fb8db8bd1c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466581031774ac8ddb27699e61f2fbf858fce357adad7352cc410ef9ad6344bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.5`

```console
$ docker pull docker@sha256:0b90b0aefd15794e4d5bea2debc3b761c1d3481a92ec7166f8453652d0deba95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.5` - linux; amd64

```console
$ docker pull docker@sha256:48db0e29e2214d564b66daffc707ad290c8788dc655cea59c605f021790d38a0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69033024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c774f62a9b520060d72c3c1901facdfdfd0fc4ae7c5e817cdaf6acd456432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:aa908727daa7433a0d156f6c6703fe5d945c4019e8b7f5d0c4fc8213e6d67fed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64511941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e68c26581b5f619c73bdd54951308df6920447f7be745bea2bfbb6b3624b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:ec6f3f2f65803962bd623ab2de639bd87d41d856c6ef477ae58383b379a1376a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fc3364d97bc6d5e8c8de60fa7c776bbc4eb6ca32c38029201f27c506086b11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e09d98b19bbee9f15b9f66604d48401833716faef061e9e509b48fb8db8bd1c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466581031774ac8ddb27699e61f2fbf858fce357adad7352cc410ef9ad6344bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.5-dind`

```console
$ docker pull docker@sha256:033ba84f8ea98910d8fc51b8263fbeb24c48d6daf55ef7c654e2981784dac2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:efd3d1db027f0c8d2cc7019b5381fc9c3cdbbda3642c3ef4feefe5a36cbf0769
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74624904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8489eeb24a264b6bcdb17f3da00140cebe92ee36bd22365f37d07d59390df4ee`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e319d9500b33aea20e9c76900595c113e652ebf38ed7021f5daf0e5d78f48af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67731913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6bc19942666d644c636de3a0210745329f07a4c2d3f32c3e9cbd7454e1228c`
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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 05:53:41 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 05:53:41 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 05:53:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 05:53:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:45 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 05:53:46 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 05:53:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:47 GMT
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6186deaef3161317f61f202acfab3875747c2a724fad1a65f29f18b068a9ca6c`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 3.2 MB (3215383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6fa6e67b938d446f54f8d3a432d35377ff3431821d39ea805fb2de790ef343`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00bcda5d341dc29b37b45898451e3133f9d420af32d36b21c94d30ac2429ed6`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 749.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daeb323203a88ce4e9152363b7ea9dc8c97580d9723309e442b2c170beb2815`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7e8985ea07f8786be5b7c551d9547aac01e43a74e8a5831685b39d40fda6d3c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67091202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef820b49fd591346a99dec34fab401da3022b7cbd60eb8d06f9baef8872d9f3`
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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:02:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 03:02:28 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 03:02:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 03:02:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 03:02:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:02:41 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 03:02:43 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 03:02:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:49 GMT
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cb30959a65f691f18075812bbdb8d5f87f944b6d8012dbce90e70e61de7c17`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 2.9 MB (2878527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4bdbf92a47a6e710c3aa65a5fbe9136e986509ab9dacdb67a196fa99441578`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ee73f368ab0a867e3f6b7294736b2ea3263dbf8cc5e6881a1b68ff5856a5c7`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0bf5e1afaa1f42f73b39a23c9e2203e65c65f6246e63d17ae6def1232a6c5b`  
		Last Modified: Sat, 18 Jan 2020 03:04:00 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31f0251cf185d41e1b6f25bf8acf3d816a73d1d8e583b4c72321a7ccc05801e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53793fffe26de8f80d9cdfa58c38018e90af8d08eb3f44ebedc03079b7d04d`
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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 02:24:11 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 02:24:13 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 02:24:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 02:24:22 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:24:25 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 02:24:26 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 02:24:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 02:24:33 GMT
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4704739272105dd3fdfc8614ba689cffe338a0faddc99dace44e191c4567ce`  
		Last Modified: Sat, 18 Jan 2020 02:26:12 GMT  
		Size: 5.6 MB (5589240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee8637fb5dd84f5ab45114fc090fda27e2eee33b46a01802c9853a3d0c1b623`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01413155fcbeedeee71c38d84c48825794515972fd5480a22210379d739d0a`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9514c7ce5d1ffef3aa0a3d41faed1d3ac1e700f99f71157dd4e7d6c418b01de`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.5-dind-rootless`

```console
$ docker pull docker@sha256:51f925a59f79f9f85b4869649f6bec7bed065f381186f4102c942ddd4a861cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:966cb6bf3b3955ebda64d4e156870e68e3ce20ac9c84a01dee28803aebc334af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97154857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384deac7f3c53083e5d29d8e56a0fa57afa7d88db3c4c34a80c774852f789d26`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
CMD []
# Sat, 18 Jan 2020 04:42:28 GMT
RUN apk add --no-cache iproute2
# Sat, 18 Jan 2020 04:42:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 18 Jan 2020 04:42:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Sat, 18 Jan 2020 04:42:32 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Sat, 18 Jan 2020 04:42:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Sat, 18 Jan 2020 04:42:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 18 Jan 2020 04:42:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 18 Jan 2020 04:42:44 GMT
USER rootless
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cdf1bd44b48b8727fa4bb0545240435dcf820156f0408b1bc13c094f8c01ea`  
		Last Modified: Sat, 18 Jan 2020 04:43:31 GMT  
		Size: 796.0 KB (795977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2313da576c87883442d37ff3743eacdb90d03a6928e9296f65a1083828ffc33`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542b530e16b9b04d347cb7c9c99bfa6e4929f67f58f26d1d74d41ab5d80ac8f2`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf525cafee47f341c3c95e742264c04417841f805670bbf8696bdcc8668082d`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f405bb85fe91994888d7507dd0641b3db43930cf575311ec56af1eead91bd`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 12.6 MB (12622917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373e62ddc7e7489f78a881fa66963be9043dc35ca8e4f345f1d7623af4444fcc`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.5-git`

```console
$ docker pull docker@sha256:8b7d15b6cf2118ec104cae6af089d5a9e25f26c687244a2ff93434d10203aa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.5-git` - linux; amd64

```console
$ docker pull docker@sha256:64c5cef8dc95f84402635d52a1970f958cec67091c18faf4ccd67eeeb53cbf08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77246911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab302e671fdaea238f1049815cb3a36f892ca5499535b6ac80cb6dddb25016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f18ea2cbac4c4171b630fa800f91a1cb433728e55ebf865c4e560df098f16d`  
		Last Modified: Sat, 18 Jan 2020 04:43:42 GMT  
		Size: 8.2 MB (8213887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7464319797cdc81c2a14d9a7c7cbf33afc28d80f08ad9c17ddf543d0d14d6d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72347135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c3149aca6d91cef011b6ae505719d9294f0cfc56f9c3ec27e89d06e5248ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:56 GMT
RUN apk add --no-cache git
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25f25e40a87dd2b1e9da8caeaa383822f1194959380646fd4b91816d0fdfb9b`  
		Last Modified: Sat, 18 Jan 2020 05:55:11 GMT  
		Size: 7.8 MB (7835194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13771936ea2943baad627ff2354ef3a37b33729054081807f03f756379891de
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71280905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10013a543102f31972358bdebe7ab2982abd88ca34247df0d6795f042eca2a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:03:02 GMT
RUN apk add --no-cache git
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febf3eb0506dfc4914c9b895325fecdb22a9f7545f259026158f6ed3e951bd0b`  
		Last Modified: Sat, 18 Jan 2020 03:04:19 GMT  
		Size: 7.1 MB (7072824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d833dbf8e852bcebee568d846c92b5dfdac913bfe5c798b9cddba14b0b0c5cb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa0741e9eec3e5cff51d73a17e11ae2068efc7c31fdb5eb995e7420e100c1af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb377abbe251ebb2800e09dd698c95aaabf1a718ab29100760305b15b5a69c`  
		Last Modified: Sat, 18 Jan 2020 02:26:34 GMT  
		Size: 8.4 MB (8406028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.6-rc1`

```console
$ docker pull docker@sha256:77efc4dd533691d951435c5f79bf6b6a63987d982cbf5f04cb003895ffba00f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.6-rc1` - linux; amd64

```console
$ docker pull docker@sha256:4b83b0e9ac1831ff9913fa6fb143952fa1e3d6789cb073eb590d5b09652fa63a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69056489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b25015a4a5dbe582e265c4db37ee8e593d99b159396a90b010dd27017bf74ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:19.03.6-rc1` - linux; arm variant v6

```console
$ docker pull docker@sha256:e22ea6a95e7a18ba4702cf79dacfcb4447b69826ff90b1d53437cef600b249de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab83376529bd59608ab0c8d863f1e773d651472e920a6c4d5a4a91084078bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:19.03.6-rc1` - linux; arm variant v7

```console
$ docker pull docker@sha256:2cb1b7691a9c3bb7c8b97fb84ca0f682b3f2d272dcccbdd5382e156a4ffcc251
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64225529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee452e50995e68daefa242a5bc5cc6d16e18fe6777f4dffef3f9651b8075aa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:19.03.6-rc1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5d10183f3deff741a34964a34a70579e9e1f55dc8545a7989270d0a3a5ae0dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62199220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6308e9bd0c2b41d5c27466f4b17ec167ffc4a2eec7e37cf3f7712eb7178682a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:19.03.6-rc1-dind`

```console
$ docker pull docker@sha256:7f81bbb44543583be6408b63dc1ddd53bb4f288cf630afbb27efc7957477186e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.6-rc1-dind` - linux; amd64

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

### `docker:19.03.6-rc1-dind` - linux; arm variant v6

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

### `docker:19.03.6-rc1-dind` - linux; arm variant v7

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

### `docker:19.03.6-rc1-dind` - linux; arm64 variant v8

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

## `docker:19.03.6-rc1-dind-rootless`

```console
$ docker pull docker@sha256:5b50889f289902d6c44ae6008576dca85509449016009990ffb33ffad418bbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.6-rc1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bb4f874f5ae095c9409e1fe08458223e6044358c4b0459a6a059006685c2fd12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2bc37e8c390302fab76a3f13b0156c00fbb1ad812d0321927fe4ab089e0d79`
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
# Wed, 29 Jan 2020 19:20:21 GMT
RUN apk add --no-cache iproute2
# Wed, 29 Jan 2020 19:20:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 29 Jan 2020 19:20:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:20:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 29 Jan 2020 19:20:24 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Wed, 29 Jan 2020 19:20:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 29 Jan 2020 19:20:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 29 Jan 2020 19:20:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 29 Jan 2020 19:20:38 GMT
USER rootless
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
	-	`sha256:054f77b99387aeb01dab6508ea4dbedc9d72f46e793f99a7ed5fcb733f8e0685`  
		Last Modified: Wed, 29 Jan 2020 19:21:42 GMT  
		Size: 796.0 KB (795993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa96072b85b46e853e2ccad6892c1ff7ecbc0831b16cf2316be7f6a77a0d0db`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b041d5c47cd20d75db2d1ef784a2415a52fa0d41f16e0e80ae43b7d71e3f9a71`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaaa07dc145f1143cecad024922dd5364978790bee84a9800e6695000b1701d`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 9.1 MB (9109450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15363c502470968a3c97795e30bfe1fda1d69bd861f8a8e80edd1e591c4ae6e`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 12.6 MB (12622893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28604bcb7c8f826857a80c62f7f3175dfa505355aed5707cf1861cee37e05867`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.6-rc1-git`

```console
$ docker pull docker@sha256:80f97c7bc81636eaeb221a27c35f11cbfcd669bbee7a82f46ce4e34d57e6f250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.6-rc1-git` - linux; amd64

```console
$ docker pull docker@sha256:cd610b256ed2ce9a7b86dd99e3ac153985970cc50b171983776d016cf67da5fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77270392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e94d4448a7eae95f3e7f354cf9be68783f0dbbff0dd67fd28bfa66e1f78fdfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:20:45 GMT
RUN apk add --no-cache git
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
	-	`sha256:32d0291d68b9301cec5f7a10673d00856afaf5a49c5b7c8aa73aa6686904b3c5`  
		Last Modified: Wed, 29 Jan 2020 19:21:50 GMT  
		Size: 8.2 MB (8213903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.6-rc1-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:23cb5c332e81065473be021cc4cb578978c2b360720b9bdf4dc78e08776f88d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72373594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fb0b8b118f16035170c09c51fd3e676e4352c6bb4d8e6a9bd960b1e195af89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:50:48 GMT
RUN apk add --no-cache git
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
	-	`sha256:08022b47c10b61b1ff4a8d57b8893f544d79f46a8f7e85276c0e3af668e5a209`  
		Last Modified: Wed, 29 Jan 2020 19:52:15 GMT  
		Size: 7.8 MB (7835217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.6-rc1-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:5767b1bd4e107712fc4d1d1dde2398c76a7dbc77ddc7f077822be92c7153c66c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71298333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75427f8f168bf0640308da96c0e4c2be6ea09adc2603fbde5be3bf28a21400f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:58:20 GMT
RUN apk add --no-cache git
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
	-	`sha256:471a3cd45774553cc0b16374e13ef596b272d43195ff73a771867e831027d153`  
		Last Modified: Wed, 29 Jan 2020 19:59:47 GMT  
		Size: 7.1 MB (7072804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.6-rc1-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47d851bbbc96d8bead3242c61faf27c2908247729034875698ed19dd0bc70a99
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70605251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2db384b528083bc719aa11d72b1dca99d427450a9e285ad2a3e686e28677f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:40:30 GMT
RUN apk add --no-cache git
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
	-	`sha256:26d7dac693752cd54704b299284d477a8147921fc7f150bcadc324642206e0c5`  
		Last Modified: Wed, 29 Jan 2020 19:41:48 GMT  
		Size: 8.4 MB (8406031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind`

```console
$ docker pull docker@sha256:033ba84f8ea98910d8fc51b8263fbeb24c48d6daf55ef7c654e2981784dac2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-dind` - linux; amd64

```console
$ docker pull docker@sha256:efd3d1db027f0c8d2cc7019b5381fc9c3cdbbda3642c3ef4feefe5a36cbf0769
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74624904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8489eeb24a264b6bcdb17f3da00140cebe92ee36bd22365f37d07d59390df4ee`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e319d9500b33aea20e9c76900595c113e652ebf38ed7021f5daf0e5d78f48af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67731913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6bc19942666d644c636de3a0210745329f07a4c2d3f32c3e9cbd7454e1228c`
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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 05:53:41 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 05:53:41 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 05:53:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 05:53:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:45 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 05:53:46 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 05:53:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:47 GMT
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6186deaef3161317f61f202acfab3875747c2a724fad1a65f29f18b068a9ca6c`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 3.2 MB (3215383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6fa6e67b938d446f54f8d3a432d35377ff3431821d39ea805fb2de790ef343`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00bcda5d341dc29b37b45898451e3133f9d420af32d36b21c94d30ac2429ed6`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 749.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daeb323203a88ce4e9152363b7ea9dc8c97580d9723309e442b2c170beb2815`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7e8985ea07f8786be5b7c551d9547aac01e43a74e8a5831685b39d40fda6d3c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67091202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef820b49fd591346a99dec34fab401da3022b7cbd60eb8d06f9baef8872d9f3`
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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:02:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 03:02:28 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 03:02:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 03:02:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 03:02:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:02:41 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 03:02:43 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 03:02:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:49 GMT
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cb30959a65f691f18075812bbdb8d5f87f944b6d8012dbce90e70e61de7c17`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 2.9 MB (2878527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4bdbf92a47a6e710c3aa65a5fbe9136e986509ab9dacdb67a196fa99441578`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ee73f368ab0a867e3f6b7294736b2ea3263dbf8cc5e6881a1b68ff5856a5c7`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0bf5e1afaa1f42f73b39a23c9e2203e65c65f6246e63d17ae6def1232a6c5b`  
		Last Modified: Sat, 18 Jan 2020 03:04:00 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31f0251cf185d41e1b6f25bf8acf3d816a73d1d8e583b4c72321a7ccc05801e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53793fffe26de8f80d9cdfa58c38018e90af8d08eb3f44ebedc03079b7d04d`
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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 02:24:11 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 02:24:13 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 02:24:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 02:24:22 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:24:25 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 02:24:26 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 02:24:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 02:24:33 GMT
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4704739272105dd3fdfc8614ba689cffe338a0faddc99dace44e191c4567ce`  
		Last Modified: Sat, 18 Jan 2020 02:26:12 GMT  
		Size: 5.6 MB (5589240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee8637fb5dd84f5ab45114fc090fda27e2eee33b46a01802c9853a3d0c1b623`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01413155fcbeedeee71c38d84c48825794515972fd5480a22210379d739d0a`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9514c7ce5d1ffef3aa0a3d41faed1d3ac1e700f99f71157dd4e7d6c418b01de`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind-rootless`

```console
$ docker pull docker@sha256:51f925a59f79f9f85b4869649f6bec7bed065f381186f4102c942ddd4a861cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:966cb6bf3b3955ebda64d4e156870e68e3ce20ac9c84a01dee28803aebc334af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97154857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384deac7f3c53083e5d29d8e56a0fa57afa7d88db3c4c34a80c774852f789d26`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
CMD []
# Sat, 18 Jan 2020 04:42:28 GMT
RUN apk add --no-cache iproute2
# Sat, 18 Jan 2020 04:42:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 18 Jan 2020 04:42:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Sat, 18 Jan 2020 04:42:32 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Sat, 18 Jan 2020 04:42:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Sat, 18 Jan 2020 04:42:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 18 Jan 2020 04:42:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 18 Jan 2020 04:42:44 GMT
USER rootless
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cdf1bd44b48b8727fa4bb0545240435dcf820156f0408b1bc13c094f8c01ea`  
		Last Modified: Sat, 18 Jan 2020 04:43:31 GMT  
		Size: 796.0 KB (795977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2313da576c87883442d37ff3743eacdb90d03a6928e9296f65a1083828ffc33`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542b530e16b9b04d347cb7c9c99bfa6e4929f67f58f26d1d74d41ab5d80ac8f2`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf525cafee47f341c3c95e742264c04417841f805670bbf8696bdcc8668082d`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f405bb85fe91994888d7507dd0641b3db43930cf575311ec56af1eead91bd`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 12.6 MB (12622917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373e62ddc7e7489f78a881fa66963be9043dc35ca8e4f345f1d7623af4444fcc`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-git`

```console
$ docker pull docker@sha256:8b7d15b6cf2118ec104cae6af089d5a9e25f26c687244a2ff93434d10203aa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-git` - linux; amd64

```console
$ docker pull docker@sha256:64c5cef8dc95f84402635d52a1970f958cec67091c18faf4ccd67eeeb53cbf08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77246911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab302e671fdaea238f1049815cb3a36f892ca5499535b6ac80cb6dddb25016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f18ea2cbac4c4171b630fa800f91a1cb433728e55ebf865c4e560df098f16d`  
		Last Modified: Sat, 18 Jan 2020 04:43:42 GMT  
		Size: 8.2 MB (8213887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7464319797cdc81c2a14d9a7c7cbf33afc28d80f08ad9c17ddf543d0d14d6d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72347135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c3149aca6d91cef011b6ae505719d9294f0cfc56f9c3ec27e89d06e5248ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:56 GMT
RUN apk add --no-cache git
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25f25e40a87dd2b1e9da8caeaa383822f1194959380646fd4b91816d0fdfb9b`  
		Last Modified: Sat, 18 Jan 2020 05:55:11 GMT  
		Size: 7.8 MB (7835194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13771936ea2943baad627ff2354ef3a37b33729054081807f03f756379891de
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71280905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10013a543102f31972358bdebe7ab2982abd88ca34247df0d6795f042eca2a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:03:02 GMT
RUN apk add --no-cache git
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febf3eb0506dfc4914c9b895325fecdb22a9f7545f259026158f6ed3e951bd0b`  
		Last Modified: Sat, 18 Jan 2020 03:04:19 GMT  
		Size: 7.1 MB (7072824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d833dbf8e852bcebee568d846c92b5dfdac913bfe5c798b9cddba14b0b0c5cb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa0741e9eec3e5cff51d73a17e11ae2068efc7c31fdb5eb995e7420e100c1af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb377abbe251ebb2800e09dd698c95aaabf1a718ab29100760305b15b5a69c`  
		Last Modified: Sat, 18 Jan 2020 02:26:34 GMT  
		Size: 8.4 MB (8406028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-rc`

```console
$ docker pull docker@sha256:77efc4dd533691d951435c5f79bf6b6a63987d982cbf5f04cb003895ffba00f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-rc` - linux; amd64

```console
$ docker pull docker@sha256:4b83b0e9ac1831ff9913fa6fb143952fa1e3d6789cb073eb590d5b09652fa63a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69056489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b25015a4a5dbe582e265c4db37ee8e593d99b159396a90b010dd27017bf74ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:19.03-rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:e22ea6a95e7a18ba4702cf79dacfcb4447b69826ff90b1d53437cef600b249de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab83376529bd59608ab0c8d863f1e773d651472e920a6c4d5a4a91084078bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:19.03-rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:2cb1b7691a9c3bb7c8b97fb84ca0f682b3f2d272dcccbdd5382e156a4ffcc251
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64225529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee452e50995e68daefa242a5bc5cc6d16e18fe6777f4dffef3f9651b8075aa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:19.03-rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5d10183f3deff741a34964a34a70579e9e1f55dc8545a7989270d0a3a5ae0dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62199220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6308e9bd0c2b41d5c27466f4b17ec167ffc4a2eec7e37cf3f7712eb7178682a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:19.03-rc-dind`

```console
$ docker pull docker@sha256:7f81bbb44543583be6408b63dc1ddd53bb4f288cf630afbb27efc7957477186e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-rc-dind` - linux; amd64

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

### `docker:19.03-rc-dind` - linux; arm variant v6

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

### `docker:19.03-rc-dind` - linux; arm variant v7

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

### `docker:19.03-rc-dind` - linux; arm64 variant v8

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

## `docker:19.03-rc-dind-rootless`

```console
$ docker pull docker@sha256:5b50889f289902d6c44ae6008576dca85509449016009990ffb33ffad418bbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bb4f874f5ae095c9409e1fe08458223e6044358c4b0459a6a059006685c2fd12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2bc37e8c390302fab76a3f13b0156c00fbb1ad812d0321927fe4ab089e0d79`
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
# Wed, 29 Jan 2020 19:20:21 GMT
RUN apk add --no-cache iproute2
# Wed, 29 Jan 2020 19:20:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 29 Jan 2020 19:20:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:20:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 29 Jan 2020 19:20:24 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Wed, 29 Jan 2020 19:20:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 29 Jan 2020 19:20:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 29 Jan 2020 19:20:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 29 Jan 2020 19:20:38 GMT
USER rootless
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
	-	`sha256:054f77b99387aeb01dab6508ea4dbedc9d72f46e793f99a7ed5fcb733f8e0685`  
		Last Modified: Wed, 29 Jan 2020 19:21:42 GMT  
		Size: 796.0 KB (795993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa96072b85b46e853e2ccad6892c1ff7ecbc0831b16cf2316be7f6a77a0d0db`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b041d5c47cd20d75db2d1ef784a2415a52fa0d41f16e0e80ae43b7d71e3f9a71`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaaa07dc145f1143cecad024922dd5364978790bee84a9800e6695000b1701d`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 9.1 MB (9109450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15363c502470968a3c97795e30bfe1fda1d69bd861f8a8e80edd1e591c4ae6e`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 12.6 MB (12622893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28604bcb7c8f826857a80c62f7f3175dfa505355aed5707cf1861cee37e05867`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-rc-git`

```console
$ docker pull docker@sha256:80f97c7bc81636eaeb221a27c35f11cbfcd669bbee7a82f46ce4e34d57e6f250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-rc-git` - linux; amd64

```console
$ docker pull docker@sha256:cd610b256ed2ce9a7b86dd99e3ac153985970cc50b171983776d016cf67da5fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77270392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e94d4448a7eae95f3e7f354cf9be68783f0dbbff0dd67fd28bfa66e1f78fdfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:20:45 GMT
RUN apk add --no-cache git
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
	-	`sha256:32d0291d68b9301cec5f7a10673d00856afaf5a49c5b7c8aa73aa6686904b3c5`  
		Last Modified: Wed, 29 Jan 2020 19:21:50 GMT  
		Size: 8.2 MB (8213903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-rc-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:23cb5c332e81065473be021cc4cb578978c2b360720b9bdf4dc78e08776f88d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72373594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fb0b8b118f16035170c09c51fd3e676e4352c6bb4d8e6a9bd960b1e195af89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:50:48 GMT
RUN apk add --no-cache git
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
	-	`sha256:08022b47c10b61b1ff4a8d57b8893f544d79f46a8f7e85276c0e3af668e5a209`  
		Last Modified: Wed, 29 Jan 2020 19:52:15 GMT  
		Size: 7.8 MB (7835217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-rc-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:5767b1bd4e107712fc4d1d1dde2398c76a7dbc77ddc7f077822be92c7153c66c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71298333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75427f8f168bf0640308da96c0e4c2be6ea09adc2603fbde5be3bf28a21400f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:58:20 GMT
RUN apk add --no-cache git
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
	-	`sha256:471a3cd45774553cc0b16374e13ef596b272d43195ff73a771867e831027d153`  
		Last Modified: Wed, 29 Jan 2020 19:59:47 GMT  
		Size: 7.1 MB (7072804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47d851bbbc96d8bead3242c61faf27c2908247729034875698ed19dd0bc70a99
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70605251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2db384b528083bc719aa11d72b1dca99d427450a9e285ad2a3e686e28677f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:40:30 GMT
RUN apk add --no-cache git
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
	-	`sha256:26d7dac693752cd54704b299284d477a8147921fc7f150bcadc324642206e0c5`  
		Last Modified: Wed, 29 Jan 2020 19:41:48 GMT  
		Size: 8.4 MB (8406031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind`

```console
$ docker pull docker@sha256:033ba84f8ea98910d8fc51b8263fbeb24c48d6daf55ef7c654e2981784dac2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-dind` - linux; amd64

```console
$ docker pull docker@sha256:efd3d1db027f0c8d2cc7019b5381fc9c3cdbbda3642c3ef4feefe5a36cbf0769
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74624904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8489eeb24a264b6bcdb17f3da00140cebe92ee36bd22365f37d07d59390df4ee`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e319d9500b33aea20e9c76900595c113e652ebf38ed7021f5daf0e5d78f48af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67731913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6bc19942666d644c636de3a0210745329f07a4c2d3f32c3e9cbd7454e1228c`
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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 05:53:41 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 05:53:41 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 05:53:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 05:53:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:45 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 05:53:46 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 05:53:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:47 GMT
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6186deaef3161317f61f202acfab3875747c2a724fad1a65f29f18b068a9ca6c`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 3.2 MB (3215383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6fa6e67b938d446f54f8d3a432d35377ff3431821d39ea805fb2de790ef343`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00bcda5d341dc29b37b45898451e3133f9d420af32d36b21c94d30ac2429ed6`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 749.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daeb323203a88ce4e9152363b7ea9dc8c97580d9723309e442b2c170beb2815`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7e8985ea07f8786be5b7c551d9547aac01e43a74e8a5831685b39d40fda6d3c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67091202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef820b49fd591346a99dec34fab401da3022b7cbd60eb8d06f9baef8872d9f3`
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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:02:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 03:02:28 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 03:02:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 03:02:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 03:02:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:02:41 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 03:02:43 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 03:02:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:49 GMT
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cb30959a65f691f18075812bbdb8d5f87f944b6d8012dbce90e70e61de7c17`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 2.9 MB (2878527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4bdbf92a47a6e710c3aa65a5fbe9136e986509ab9dacdb67a196fa99441578`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ee73f368ab0a867e3f6b7294736b2ea3263dbf8cc5e6881a1b68ff5856a5c7`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0bf5e1afaa1f42f73b39a23c9e2203e65c65f6246e63d17ae6def1232a6c5b`  
		Last Modified: Sat, 18 Jan 2020 03:04:00 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31f0251cf185d41e1b6f25bf8acf3d816a73d1d8e583b4c72321a7ccc05801e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53793fffe26de8f80d9cdfa58c38018e90af8d08eb3f44ebedc03079b7d04d`
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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 02:24:11 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 02:24:13 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 02:24:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 02:24:22 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:24:25 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 02:24:26 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 02:24:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 02:24:33 GMT
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4704739272105dd3fdfc8614ba689cffe338a0faddc99dace44e191c4567ce`  
		Last Modified: Sat, 18 Jan 2020 02:26:12 GMT  
		Size: 5.6 MB (5589240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee8637fb5dd84f5ab45114fc090fda27e2eee33b46a01802c9853a3d0c1b623`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01413155fcbeedeee71c38d84c48825794515972fd5480a22210379d739d0a`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9514c7ce5d1ffef3aa0a3d41faed1d3ac1e700f99f71157dd4e7d6c418b01de`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:51f925a59f79f9f85b4869649f6bec7bed065f381186f4102c942ddd4a861cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:966cb6bf3b3955ebda64d4e156870e68e3ce20ac9c84a01dee28803aebc334af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97154857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384deac7f3c53083e5d29d8e56a0fa57afa7d88db3c4c34a80c774852f789d26`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
CMD []
# Sat, 18 Jan 2020 04:42:28 GMT
RUN apk add --no-cache iproute2
# Sat, 18 Jan 2020 04:42:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 18 Jan 2020 04:42:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Sat, 18 Jan 2020 04:42:32 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Sat, 18 Jan 2020 04:42:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Sat, 18 Jan 2020 04:42:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 18 Jan 2020 04:42:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 18 Jan 2020 04:42:44 GMT
USER rootless
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cdf1bd44b48b8727fa4bb0545240435dcf820156f0408b1bc13c094f8c01ea`  
		Last Modified: Sat, 18 Jan 2020 04:43:31 GMT  
		Size: 796.0 KB (795977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2313da576c87883442d37ff3743eacdb90d03a6928e9296f65a1083828ffc33`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542b530e16b9b04d347cb7c9c99bfa6e4929f67f58f26d1d74d41ab5d80ac8f2`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf525cafee47f341c3c95e742264c04417841f805670bbf8696bdcc8668082d`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f405bb85fe91994888d7507dd0641b3db43930cf575311ec56af1eead91bd`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 12.6 MB (12622917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373e62ddc7e7489f78a881fa66963be9043dc35ca8e4f345f1d7623af4444fcc`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-git`

```console
$ docker pull docker@sha256:8b7d15b6cf2118ec104cae6af089d5a9e25f26c687244a2ff93434d10203aa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-git` - linux; amd64

```console
$ docker pull docker@sha256:64c5cef8dc95f84402635d52a1970f958cec67091c18faf4ccd67eeeb53cbf08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77246911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab302e671fdaea238f1049815cb3a36f892ca5499535b6ac80cb6dddb25016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f18ea2cbac4c4171b630fa800f91a1cb433728e55ebf865c4e560df098f16d`  
		Last Modified: Sat, 18 Jan 2020 04:43:42 GMT  
		Size: 8.2 MB (8213887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7464319797cdc81c2a14d9a7c7cbf33afc28d80f08ad9c17ddf543d0d14d6d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72347135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c3149aca6d91cef011b6ae505719d9294f0cfc56f9c3ec27e89d06e5248ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:56 GMT
RUN apk add --no-cache git
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25f25e40a87dd2b1e9da8caeaa383822f1194959380646fd4b91816d0fdfb9b`  
		Last Modified: Sat, 18 Jan 2020 05:55:11 GMT  
		Size: 7.8 MB (7835194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13771936ea2943baad627ff2354ef3a37b33729054081807f03f756379891de
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71280905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10013a543102f31972358bdebe7ab2982abd88ca34247df0d6795f042eca2a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:03:02 GMT
RUN apk add --no-cache git
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febf3eb0506dfc4914c9b895325fecdb22a9f7545f259026158f6ed3e951bd0b`  
		Last Modified: Sat, 18 Jan 2020 03:04:19 GMT  
		Size: 7.1 MB (7072824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d833dbf8e852bcebee568d846c92b5dfdac913bfe5c798b9cddba14b0b0c5cb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa0741e9eec3e5cff51d73a17e11ae2068efc7c31fdb5eb995e7420e100c1af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb377abbe251ebb2800e09dd698c95aaabf1a718ab29100760305b15b5a69c`  
		Last Modified: Sat, 18 Jan 2020 02:26:34 GMT  
		Size: 8.4 MB (8406028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:033ba84f8ea98910d8fc51b8263fbeb24c48d6daf55ef7c654e2981784dac2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:efd3d1db027f0c8d2cc7019b5381fc9c3cdbbda3642c3ef4feefe5a36cbf0769
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74624904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8489eeb24a264b6bcdb17f3da00140cebe92ee36bd22365f37d07d59390df4ee`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e319d9500b33aea20e9c76900595c113e652ebf38ed7021f5daf0e5d78f48af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67731913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6bc19942666d644c636de3a0210745329f07a4c2d3f32c3e9cbd7454e1228c`
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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 05:53:41 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 05:53:41 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 05:53:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 05:53:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:45 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 05:53:46 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 05:53:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:47 GMT
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6186deaef3161317f61f202acfab3875747c2a724fad1a65f29f18b068a9ca6c`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 3.2 MB (3215383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6fa6e67b938d446f54f8d3a432d35377ff3431821d39ea805fb2de790ef343`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00bcda5d341dc29b37b45898451e3133f9d420af32d36b21c94d30ac2429ed6`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 749.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daeb323203a88ce4e9152363b7ea9dc8c97580d9723309e442b2c170beb2815`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7e8985ea07f8786be5b7c551d9547aac01e43a74e8a5831685b39d40fda6d3c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67091202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef820b49fd591346a99dec34fab401da3022b7cbd60eb8d06f9baef8872d9f3`
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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:02:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 03:02:28 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 03:02:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 03:02:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 03:02:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:02:41 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 03:02:43 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 03:02:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:49 GMT
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cb30959a65f691f18075812bbdb8d5f87f944b6d8012dbce90e70e61de7c17`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 2.9 MB (2878527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4bdbf92a47a6e710c3aa65a5fbe9136e986509ab9dacdb67a196fa99441578`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ee73f368ab0a867e3f6b7294736b2ea3263dbf8cc5e6881a1b68ff5856a5c7`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0bf5e1afaa1f42f73b39a23c9e2203e65c65f6246e63d17ae6def1232a6c5b`  
		Last Modified: Sat, 18 Jan 2020 03:04:00 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31f0251cf185d41e1b6f25bf8acf3d816a73d1d8e583b4c72321a7ccc05801e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53793fffe26de8f80d9cdfa58c38018e90af8d08eb3f44ebedc03079b7d04d`
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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 02:24:11 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 02:24:13 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 02:24:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 02:24:22 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:24:25 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 02:24:26 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 02:24:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 02:24:33 GMT
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4704739272105dd3fdfc8614ba689cffe338a0faddc99dace44e191c4567ce`  
		Last Modified: Sat, 18 Jan 2020 02:26:12 GMT  
		Size: 5.6 MB (5589240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee8637fb5dd84f5ab45114fc090fda27e2eee33b46a01802c9853a3d0c1b623`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01413155fcbeedeee71c38d84c48825794515972fd5480a22210379d739d0a`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9514c7ce5d1ffef3aa0a3d41faed1d3ac1e700f99f71157dd4e7d6c418b01de`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:51f925a59f79f9f85b4869649f6bec7bed065f381186f4102c942ddd4a861cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:966cb6bf3b3955ebda64d4e156870e68e3ce20ac9c84a01dee28803aebc334af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97154857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384deac7f3c53083e5d29d8e56a0fa57afa7d88db3c4c34a80c774852f789d26`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
CMD []
# Sat, 18 Jan 2020 04:42:28 GMT
RUN apk add --no-cache iproute2
# Sat, 18 Jan 2020 04:42:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 18 Jan 2020 04:42:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Sat, 18 Jan 2020 04:42:32 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Sat, 18 Jan 2020 04:42:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Sat, 18 Jan 2020 04:42:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 18 Jan 2020 04:42:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 18 Jan 2020 04:42:44 GMT
USER rootless
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cdf1bd44b48b8727fa4bb0545240435dcf820156f0408b1bc13c094f8c01ea`  
		Last Modified: Sat, 18 Jan 2020 04:43:31 GMT  
		Size: 796.0 KB (795977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2313da576c87883442d37ff3743eacdb90d03a6928e9296f65a1083828ffc33`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542b530e16b9b04d347cb7c9c99bfa6e4929f67f58f26d1d74d41ab5d80ac8f2`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf525cafee47f341c3c95e742264c04417841f805670bbf8696bdcc8668082d`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f405bb85fe91994888d7507dd0641b3db43930cf575311ec56af1eead91bd`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 12.6 MB (12622917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373e62ddc7e7489f78a881fa66963be9043dc35ca8e4f345f1d7623af4444fcc`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:8b7d15b6cf2118ec104cae6af089d5a9e25f26c687244a2ff93434d10203aa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:64c5cef8dc95f84402635d52a1970f958cec67091c18faf4ccd67eeeb53cbf08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77246911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab302e671fdaea238f1049815cb3a36f892ca5499535b6ac80cb6dddb25016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f18ea2cbac4c4171b630fa800f91a1cb433728e55ebf865c4e560df098f16d`  
		Last Modified: Sat, 18 Jan 2020 04:43:42 GMT  
		Size: 8.2 MB (8213887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7464319797cdc81c2a14d9a7c7cbf33afc28d80f08ad9c17ddf543d0d14d6d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72347135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c3149aca6d91cef011b6ae505719d9294f0cfc56f9c3ec27e89d06e5248ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:56 GMT
RUN apk add --no-cache git
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25f25e40a87dd2b1e9da8caeaa383822f1194959380646fd4b91816d0fdfb9b`  
		Last Modified: Sat, 18 Jan 2020 05:55:11 GMT  
		Size: 7.8 MB (7835194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13771936ea2943baad627ff2354ef3a37b33729054081807f03f756379891de
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71280905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10013a543102f31972358bdebe7ab2982abd88ca34247df0d6795f042eca2a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:03:02 GMT
RUN apk add --no-cache git
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febf3eb0506dfc4914c9b895325fecdb22a9f7545f259026158f6ed3e951bd0b`  
		Last Modified: Sat, 18 Jan 2020 03:04:19 GMT  
		Size: 7.1 MB (7072824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d833dbf8e852bcebee568d846c92b5dfdac913bfe5c798b9cddba14b0b0c5cb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa0741e9eec3e5cff51d73a17e11ae2068efc7c31fdb5eb995e7420e100c1af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb377abbe251ebb2800e09dd698c95aaabf1a718ab29100760305b15b5a69c`  
		Last Modified: Sat, 18 Jan 2020 02:26:34 GMT  
		Size: 8.4 MB (8406028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:0b90b0aefd15794e4d5bea2debc3b761c1d3481a92ec7166f8453652d0deba95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:48db0e29e2214d564b66daffc707ad290c8788dc655cea59c605f021790d38a0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69033024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c774f62a9b520060d72c3c1901facdfdfd0fc4ae7c5e817cdaf6acd456432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:aa908727daa7433a0d156f6c6703fe5d945c4019e8b7f5d0c4fc8213e6d67fed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64511941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e68c26581b5f619c73bdd54951308df6920447f7be745bea2bfbb6b3624b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:ec6f3f2f65803962bd623ab2de639bd87d41d856c6ef477ae58383b379a1376a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fc3364d97bc6d5e8c8de60fa7c776bbc4eb6ca32c38029201f27c506086b11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e09d98b19bbee9f15b9f66604d48401833716faef061e9e509b48fb8db8bd1c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466581031774ac8ddb27699e61f2fbf858fce357adad7352cc410ef9ad6344bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc`

```console
$ docker pull docker@sha256:77efc4dd533691d951435c5f79bf6b6a63987d982cbf5f04cb003895ffba00f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:4b83b0e9ac1831ff9913fa6fb143952fa1e3d6789cb073eb590d5b09652fa63a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69056489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b25015a4a5dbe582e265c4db37ee8e593d99b159396a90b010dd27017bf74ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:e22ea6a95e7a18ba4702cf79dacfcb4447b69826ff90b1d53437cef600b249de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab83376529bd59608ab0c8d863f1e773d651472e920a6c4d5a4a91084078bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:2cb1b7691a9c3bb7c8b97fb84ca0f682b3f2d272dcccbdd5382e156a4ffcc251
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64225529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee452e50995e68daefa242a5bc5cc6d16e18fe6777f4dffef3f9651b8075aa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5d10183f3deff741a34964a34a70579e9e1f55dc8545a7989270d0a3a5ae0dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62199220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6308e9bd0c2b41d5c27466f4b17ec167ffc4a2eec7e37cf3f7712eb7178682a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:5b50889f289902d6c44ae6008576dca85509449016009990ffb33ffad418bbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bb4f874f5ae095c9409e1fe08458223e6044358c4b0459a6a059006685c2fd12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2bc37e8c390302fab76a3f13b0156c00fbb1ad812d0321927fe4ab089e0d79`
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
# Wed, 29 Jan 2020 19:20:21 GMT
RUN apk add --no-cache iproute2
# Wed, 29 Jan 2020 19:20:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 29 Jan 2020 19:20:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:20:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 29 Jan 2020 19:20:24 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Wed, 29 Jan 2020 19:20:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 29 Jan 2020 19:20:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 29 Jan 2020 19:20:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 29 Jan 2020 19:20:38 GMT
USER rootless
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
	-	`sha256:054f77b99387aeb01dab6508ea4dbedc9d72f46e793f99a7ed5fcb733f8e0685`  
		Last Modified: Wed, 29 Jan 2020 19:21:42 GMT  
		Size: 796.0 KB (795993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa96072b85b46e853e2ccad6892c1ff7ecbc0831b16cf2316be7f6a77a0d0db`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b041d5c47cd20d75db2d1ef784a2415a52fa0d41f16e0e80ae43b7d71e3f9a71`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaaa07dc145f1143cecad024922dd5364978790bee84a9800e6695000b1701d`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 9.1 MB (9109450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15363c502470968a3c97795e30bfe1fda1d69bd861f8a8e80edd1e591c4ae6e`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 12.6 MB (12622893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28604bcb7c8f826857a80c62f7f3175dfa505355aed5707cf1861cee37e05867`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-git`

```console
$ docker pull docker@sha256:80f97c7bc81636eaeb221a27c35f11cbfcd669bbee7a82f46ce4e34d57e6f250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:cd610b256ed2ce9a7b86dd99e3ac153985970cc50b171983776d016cf67da5fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77270392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e94d4448a7eae95f3e7f354cf9be68783f0dbbff0dd67fd28bfa66e1f78fdfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:20:45 GMT
RUN apk add --no-cache git
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
	-	`sha256:32d0291d68b9301cec5f7a10673d00856afaf5a49c5b7c8aa73aa6686904b3c5`  
		Last Modified: Wed, 29 Jan 2020 19:21:50 GMT  
		Size: 8.2 MB (8213903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:23cb5c332e81065473be021cc4cb578978c2b360720b9bdf4dc78e08776f88d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72373594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fb0b8b118f16035170c09c51fd3e676e4352c6bb4d8e6a9bd960b1e195af89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:50:48 GMT
RUN apk add --no-cache git
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
	-	`sha256:08022b47c10b61b1ff4a8d57b8893f544d79f46a8f7e85276c0e3af668e5a209`  
		Last Modified: Wed, 29 Jan 2020 19:52:15 GMT  
		Size: 7.8 MB (7835217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:5767b1bd4e107712fc4d1d1dde2398c76a7dbc77ddc7f077822be92c7153c66c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71298333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75427f8f168bf0640308da96c0e4c2be6ea09adc2603fbde5be3bf28a21400f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:58:20 GMT
RUN apk add --no-cache git
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
	-	`sha256:471a3cd45774553cc0b16374e13ef596b272d43195ff73a771867e831027d153`  
		Last Modified: Wed, 29 Jan 2020 19:59:47 GMT  
		Size: 7.1 MB (7072804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47d851bbbc96d8bead3242c61faf27c2908247729034875698ed19dd0bc70a99
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70605251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2db384b528083bc719aa11d72b1dca99d427450a9e285ad2a3e686e28677f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:40:30 GMT
RUN apk add --no-cache git
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
	-	`sha256:26d7dac693752cd54704b299284d477a8147921fc7f150bcadc324642206e0c5`  
		Last Modified: Wed, 29 Jan 2020 19:41:48 GMT  
		Size: 8.4 MB (8406031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable`

```console
$ docker pull docker@sha256:0b90b0aefd15794e4d5bea2debc3b761c1d3481a92ec7166f8453652d0deba95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable` - linux; amd64

```console
$ docker pull docker@sha256:48db0e29e2214d564b66daffc707ad290c8788dc655cea59c605f021790d38a0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69033024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c774f62a9b520060d72c3c1901facdfdfd0fc4ae7c5e817cdaf6acd456432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v6

```console
$ docker pull docker@sha256:aa908727daa7433a0d156f6c6703fe5d945c4019e8b7f5d0c4fc8213e6d67fed
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64511941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e68c26581b5f619c73bdd54951308df6920447f7be745bea2bfbb6b3624b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v7

```console
$ docker pull docker@sha256:ec6f3f2f65803962bd623ab2de639bd87d41d856c6ef477ae58383b379a1376a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64208081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fc3364d97bc6d5e8c8de60fa7c776bbc4eb6ca32c38029201f27c506086b11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e09d98b19bbee9f15b9f66604d48401833716faef061e9e509b48fb8db8bd1c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62176875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466581031774ac8ddb27699e61f2fbf858fce357adad7352cc410ef9ad6344bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-dind`

```console
$ docker pull docker@sha256:033ba84f8ea98910d8fc51b8263fbeb24c48d6daf55ef7c654e2981784dac2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-dind` - linux; amd64

```console
$ docker pull docker@sha256:efd3d1db027f0c8d2cc7019b5381fc9c3cdbbda3642c3ef4feefe5a36cbf0769
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74624904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8489eeb24a264b6bcdb17f3da00140cebe92ee36bd22365f37d07d59390df4ee`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e319d9500b33aea20e9c76900595c113e652ebf38ed7021f5daf0e5d78f48af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67731913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6bc19942666d644c636de3a0210745329f07a4c2d3f32c3e9cbd7454e1228c`
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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 05:53:41 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 05:53:41 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 05:53:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 05:53:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:45 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 05:53:46 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 05:53:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:47 GMT
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6186deaef3161317f61f202acfab3875747c2a724fad1a65f29f18b068a9ca6c`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 3.2 MB (3215383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6fa6e67b938d446f54f8d3a432d35377ff3431821d39ea805fb2de790ef343`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00bcda5d341dc29b37b45898451e3133f9d420af32d36b21c94d30ac2429ed6`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 749.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daeb323203a88ce4e9152363b7ea9dc8c97580d9723309e442b2c170beb2815`  
		Last Modified: Sat, 18 Jan 2020 05:54:54 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7e8985ea07f8786be5b7c551d9547aac01e43a74e8a5831685b39d40fda6d3c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67091202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef820b49fd591346a99dec34fab401da3022b7cbd60eb8d06f9baef8872d9f3`
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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:02:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 03:02:28 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 03:02:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 03:02:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 03:02:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:02:41 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 03:02:43 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 03:02:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:49 GMT
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cb30959a65f691f18075812bbdb8d5f87f944b6d8012dbce90e70e61de7c17`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 2.9 MB (2878527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4bdbf92a47a6e710c3aa65a5fbe9136e986509ab9dacdb67a196fa99441578`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ee73f368ab0a867e3f6b7294736b2ea3263dbf8cc5e6881a1b68ff5856a5c7`  
		Last Modified: Sat, 18 Jan 2020 03:03:59 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0bf5e1afaa1f42f73b39a23c9e2203e65c65f6246e63d17ae6def1232a6c5b`  
		Last Modified: Sat, 18 Jan 2020 03:04:00 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31f0251cf185d41e1b6f25bf8acf3d816a73d1d8e583b4c72321a7ccc05801e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53793fffe26de8f80d9cdfa58c38018e90af8d08eb3f44ebedc03079b7d04d`
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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 02:24:11 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 02:24:13 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 02:24:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 02:24:22 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:24:25 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 02:24:26 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 02:24:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 02:24:33 GMT
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4704739272105dd3fdfc8614ba689cffe338a0faddc99dace44e191c4567ce`  
		Last Modified: Sat, 18 Jan 2020 02:26:12 GMT  
		Size: 5.6 MB (5589240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee8637fb5dd84f5ab45114fc090fda27e2eee33b46a01802c9853a3d0c1b623`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01413155fcbeedeee71c38d84c48825794515972fd5480a22210379d739d0a`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9514c7ce5d1ffef3aa0a3d41faed1d3ac1e700f99f71157dd4e7d6c418b01de`  
		Last Modified: Sat, 18 Jan 2020 02:26:10 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-dind-rootless`

```console
$ docker pull docker@sha256:51f925a59f79f9f85b4869649f6bec7bed065f381186f4102c942ddd4a861cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:stable-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:966cb6bf3b3955ebda64d4e156870e68e3ce20ac9c84a01dee28803aebc334af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97154857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384deac7f3c53083e5d29d8e56a0fa57afa7d88db3c4c34a80c774852f789d26`
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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 18 Jan 2020 04:42:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Sat, 18 Jan 2020 04:42:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 18 Jan 2020 04:42:23 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:23 GMT
VOLUME [/var/lib/docker]
# Sat, 18 Jan 2020 04:42:23 GMT
EXPOSE 2375 2376
# Sat, 18 Jan 2020 04:42:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:24 GMT
CMD []
# Sat, 18 Jan 2020 04:42:28 GMT
RUN apk add --no-cache iproute2
# Sat, 18 Jan 2020 04:42:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 18 Jan 2020 04:42:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 18 Jan 2020 04:42:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Sat, 18 Jan 2020 04:42:32 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Sat, 18 Jan 2020 04:42:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Sat, 18 Jan 2020 04:42:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 18 Jan 2020 04:42:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 18 Jan 2020 04:42:44 GMT
USER rootless
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a997a372dbd0d87870fa25eae7215255eb2b01d9e29628131bc069ec6881d51`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 5.6 MB (5587312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab6c938e0f206309b6694d77374fe49f8885b0ecd70255ff85f20b0ba5958c`  
		Last Modified: Sat, 18 Jan 2020 04:43:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fcc3f54ae1a83af62f345563b1dfa6b0ae7b0a7b41a29cae54b519c920fc39`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8202733384404f005b36e4dd532c29869dc6d52131d69cb7c3970906f62a81`  
		Last Modified: Sat, 18 Jan 2020 04:43:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cdf1bd44b48b8727fa4bb0545240435dcf820156f0408b1bc13c094f8c01ea`  
		Last Modified: Sat, 18 Jan 2020 04:43:31 GMT  
		Size: 796.0 KB (795977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2313da576c87883442d37ff3743eacdb90d03a6928e9296f65a1083828ffc33`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542b530e16b9b04d347cb7c9c99bfa6e4929f67f58f26d1d74d41ab5d80ac8f2`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf525cafee47f341c3c95e742264c04417841f805670bbf8696bdcc8668082d`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2f405bb85fe91994888d7507dd0641b3db43930cf575311ec56af1eead91bd`  
		Last Modified: Sat, 18 Jan 2020 04:43:32 GMT  
		Size: 12.6 MB (12622917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373e62ddc7e7489f78a881fa66963be9043dc35ca8e4f345f1d7623af4444fcc`  
		Last Modified: Sat, 18 Jan 2020 04:43:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-git`

```console
$ docker pull docker@sha256:8b7d15b6cf2118ec104cae6af089d5a9e25f26c687244a2ff93434d10203aa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-git` - linux; amd64

```console
$ docker pull docker@sha256:64c5cef8dc95f84402635d52a1970f958cec67091c18faf4ccd67eeeb53cbf08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77246911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab302e671fdaea238f1049815cb3a36f892ca5499535b6ac80cb6dddb25016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 04:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 04:42:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 04:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 04:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 04:42:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 04:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 04:42:15 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 04:42:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:79e322b40fa78bcb793fcabe57869cfb5e210bb5cfc275064f0cfbe427a36e4e`  
		Last Modified: Sat, 18 Jan 2020 04:43:14 GMT  
		Size: 63.8 MB (63803085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa396aa1c77a2fdb0f6c0ac033a521f8de6ead46ba5d705165277cc5941eda4d`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b1978c51ebb57ab388b7b3c5a9f6590b49dc4d66b2975074b47a92a56c67c`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cc93a7c6112de21c1587c24848731a1ebe1fb72cd8c70179311490b881d6cb`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f18ea2cbac4c4171b630fa800f91a1cb433728e55ebf865c4e560df098f16d`  
		Last Modified: Sat, 18 Jan 2020 04:43:42 GMT  
		Size: 8.2 MB (8213887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7464319797cdc81c2a14d9a7c7cbf33afc28d80f08ad9c17ddf543d0d14d6d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72347135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c3149aca6d91cef011b6ae505719d9294f0cfc56f9c3ec27e89d06e5248ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 05:52:39 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 05:53:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 05:53:01 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 05:53:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 05:53:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 05:53:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 05:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 05:53:22 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 05:53:56 GMT
RUN apk add --no-cache git
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
	-	`sha256:b2b67a1db9eac111453ec819e686eb891049a6f159178b5e9b3d09c31fd30f26`  
		Last Modified: Sat, 18 Jan 2020 05:54:40 GMT  
		Size: 59.5 MB (59537111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec15d907cba1cc3d6cce4ab1bdd3a7dc51f47536ee2cee27045d33874c14a46`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3737ec4c19552130a00ec7865542544cfa894f2a8db7d0af66f5d7f689f60`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce6c271f4e453a31d10d27ae7e3293e9cd064155a53dca693672a455cd4654`  
		Last Modified: Sat, 18 Jan 2020 05:54:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25f25e40a87dd2b1e9da8caeaa383822f1194959380646fd4b91816d0fdfb9b`  
		Last Modified: Sat, 18 Jan 2020 05:55:11 GMT  
		Size: 7.8 MB (7835194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13771936ea2943baad627ff2354ef3a37b33729054081807f03f756379891de
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71280905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10013a543102f31972358bdebe7ab2982abd88ca34247df0d6795f042eca2a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 03:01:23 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 03:01:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 03:01:50 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 03:01:51 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 03:01:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 03:02:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 03:02:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 03:02:04 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 03:03:02 GMT
RUN apk add --no-cache git
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
	-	`sha256:326615998585f23d6e965ad3a7c5ae78ad6751b00d515729fbe5b6812253c7ef`  
		Last Modified: Sat, 18 Jan 2020 03:03:44 GMT  
		Size: 59.5 MB (59532265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2babc205ada15798696c663e276d3e030c340387254b459937fd034f901ae6`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca461e06d78610e28ccb1e7164387cdd443dbe0c28876aa1ff1af27083240a`  
		Last Modified: Sat, 18 Jan 2020 03:03:24 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c6de963ff509e6c53b701cfe9c9410e7d346c8433079189a2cb394f6ae247`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febf3eb0506dfc4914c9b895325fecdb22a9f7545f259026158f6ed3e951bd0b`  
		Last Modified: Sat, 18 Jan 2020 03:04:19 GMT  
		Size: 7.1 MB (7072824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d833dbf8e852bcebee568d846c92b5dfdac913bfe5c798b9cddba14b0b0c5cb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa0741e9eec3e5cff51d73a17e11ae2068efc7c31fdb5eb995e7420e100c1af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Sat, 18 Jan 2020 02:23:13 GMT
ENV DOCKER_VERSION=19.03.5
# Sat, 18 Jan 2020 02:23:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Sat, 18 Jan 2020 02:23:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 18 Jan 2020 02:23:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 18 Jan 2020 02:23:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 18 Jan 2020 02:23:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 18 Jan 2020 02:23:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Jan 2020 02:23:44 GMT
CMD ["sh"]
# Sat, 18 Jan 2020 02:24:50 GMT
RUN apk add --no-cache git
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
	-	`sha256:32738a03c1ca50289bdc7d81b64edd2af2a130c1d1d742a8cd81e63c9306aff7`  
		Last Modified: Sat, 18 Jan 2020 02:25:52 GMT  
		Size: 57.0 MB (57006218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36258bdcaf02f467a616cd09eafc78bef2d8343cfd373ade6678cc2669b376e`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149292bf8308cae48ff11692e17ff1e42f4627983b20838d43c9ff7daf0fc23a`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91f03656c5246a841a4caf06f518776b95c9fc77409342bc082fa7eaacfe3bb`  
		Last Modified: Sat, 18 Jan 2020 02:25:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb377abbe251ebb2800e09dd698c95aaabf1a718ab29100760305b15b5a69c`  
		Last Modified: Sat, 18 Jan 2020 02:26:34 GMT  
		Size: 8.4 MB (8406028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test`

```console
$ docker pull docker@sha256:77efc4dd533691d951435c5f79bf6b6a63987d982cbf5f04cb003895ffba00f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test` - linux; amd64

```console
$ docker pull docker@sha256:4b83b0e9ac1831ff9913fa6fb143952fa1e3d6789cb073eb590d5b09652fa63a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69056489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b25015a4a5dbe582e265c4db37ee8e593d99b159396a90b010dd27017bf74ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:test` - linux; arm variant v6

```console
$ docker pull docker@sha256:e22ea6a95e7a18ba4702cf79dacfcb4447b69826ff90b1d53437cef600b249de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64538377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab83376529bd59608ab0c8d863f1e773d651472e920a6c4d5a4a91084078bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:test` - linux; arm variant v7

```console
$ docker pull docker@sha256:2cb1b7691a9c3bb7c8b97fb84ca0f682b3f2d272dcccbdd5382e156a4ffcc251
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64225529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee452e50995e68daefa242a5bc5cc6d16e18fe6777f4dffef3f9651b8075aa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:test` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5d10183f3deff741a34964a34a70579e9e1f55dc8545a7989270d0a3a5ae0dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62199220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6308e9bd0c2b41d5c27466f4b17ec167ffc4a2eec7e37cf3f7712eb7178682a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:test-dind`

```console
$ docker pull docker@sha256:7f81bbb44543583be6408b63dc1ddd53bb4f288cf630afbb27efc7957477186e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-dind` - linux; amd64

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

### `docker:test-dind` - linux; arm variant v6

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

### `docker:test-dind` - linux; arm variant v7

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

### `docker:test-dind` - linux; arm64 variant v8

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

## `docker:test-dind-rootless`

```console
$ docker pull docker@sha256:5b50889f289902d6c44ae6008576dca85509449016009990ffb33ffad418bbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:test-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bb4f874f5ae095c9409e1fe08458223e6044358c4b0459a6a059006685c2fd12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2bc37e8c390302fab76a3f13b0156c00fbb1ad812d0321927fe4ab089e0d79`
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
# Wed, 29 Jan 2020 19:20:21 GMT
RUN apk add --no-cache iproute2
# Wed, 29 Jan 2020 19:20:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 29 Jan 2020 19:20:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 29 Jan 2020 19:20:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 29 Jan 2020 19:20:24 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Wed, 29 Jan 2020 19:20:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 29 Jan 2020 19:20:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 29 Jan 2020 19:20:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 29 Jan 2020 19:20:38 GMT
USER rootless
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
	-	`sha256:054f77b99387aeb01dab6508ea4dbedc9d72f46e793f99a7ed5fcb733f8e0685`  
		Last Modified: Wed, 29 Jan 2020 19:21:42 GMT  
		Size: 796.0 KB (795993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa96072b85b46e853e2ccad6892c1ff7ecbc0831b16cf2316be7f6a77a0d0db`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b041d5c47cd20d75db2d1ef784a2415a52fa0d41f16e0e80ae43b7d71e3f9a71`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaaa07dc145f1143cecad024922dd5364978790bee84a9800e6695000b1701d`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 9.1 MB (9109450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15363c502470968a3c97795e30bfe1fda1d69bd861f8a8e80edd1e591c4ae6e`  
		Last Modified: Wed, 29 Jan 2020 19:21:44 GMT  
		Size: 12.6 MB (12622893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28604bcb7c8f826857a80c62f7f3175dfa505355aed5707cf1861cee37e05867`  
		Last Modified: Wed, 29 Jan 2020 19:21:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-git`

```console
$ docker pull docker@sha256:80f97c7bc81636eaeb221a27c35f11cbfcd669bbee7a82f46ce4e34d57e6f250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-git` - linux; amd64

```console
$ docker pull docker@sha256:cd610b256ed2ce9a7b86dd99e3ac153985970cc50b171983776d016cf67da5fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77270392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e94d4448a7eae95f3e7f354cf9be68783f0dbbff0dd67fd28bfa66e1f78fdfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:20:45 GMT
RUN apk add --no-cache git
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
	-	`sha256:32d0291d68b9301cec5f7a10673d00856afaf5a49c5b7c8aa73aa6686904b3c5`  
		Last Modified: Wed, 29 Jan 2020 19:21:50 GMT  
		Size: 8.2 MB (8213903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:23cb5c332e81065473be021cc4cb578978c2b360720b9bdf4dc78e08776f88d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72373594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fb0b8b118f16035170c09c51fd3e676e4352c6bb4d8e6a9bd960b1e195af89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:50:48 GMT
RUN apk add --no-cache git
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
	-	`sha256:08022b47c10b61b1ff4a8d57b8893f544d79f46a8f7e85276c0e3af668e5a209`  
		Last Modified: Wed, 29 Jan 2020 19:52:15 GMT  
		Size: 7.8 MB (7835217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:5767b1bd4e107712fc4d1d1dde2398c76a7dbc77ddc7f077822be92c7153c66c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71298333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75427f8f168bf0640308da96c0e4c2be6ea09adc2603fbde5be3bf28a21400f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:58:20 GMT
RUN apk add --no-cache git
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
	-	`sha256:471a3cd45774553cc0b16374e13ef596b272d43195ff73a771867e831027d153`  
		Last Modified: Wed, 29 Jan 2020 19:59:47 GMT  
		Size: 7.1 MB (7072804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47d851bbbc96d8bead3242c61faf27c2908247729034875698ed19dd0bc70a99
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70605251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2db384b528083bc719aa11d72b1dca99d427450a9e285ad2a3e686e28677f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 29 Jan 2020 19:40:30 GMT
RUN apk add --no-cache git
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
	-	`sha256:26d7dac693752cd54704b299284d477a8147921fc7f150bcadc324642206e0c5`  
		Last Modified: Wed, 29 Jan 2020 19:41:48 GMT  
		Size: 8.4 MB (8406031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:19`](#docker19)
-	[`docker:19.03`](#docker1903)
-	[`docker:19.03.5`](#docker19035)
-	[`docker:19.03.5-dind`](#docker19035-dind)
-	[`docker:19.03.5-dind-rootless`](#docker19035-dind-rootless)
-	[`docker:19.03.5-git`](#docker19035-git)
-	[`docker:19.03-dind`](#docker1903-dind)
-	[`docker:19.03-dind-rootless`](#docker1903-dind-rootless)
-	[`docker:19.03-git`](#docker1903-git)
-	[`docker:19-dind`](#docker19-dind)
-	[`docker:19-dind-rootless`](#docker19-dind-rootless)
-	[`docker:19-git`](#docker19-git)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
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
$ docker pull docker@sha256:9f3ebcd963a0cfdf6d6a9d7ed0554e008343ca473b85d738527b763288ddb32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19` - linux; amd64

```console
$ docker pull docker@sha256:83a5911718a8e472a56f615f2939358508dfc6f6f0eaa460ef58460d7c18d723
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dab1a583eeee3300a1ff1fb14e75e0ab7cf2d4afb03c54801358fd3551e86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v6

```console
$ docker pull docker@sha256:d9e5bdce93b32511f9a1573e12db70984ece850504dd844af758a3cec1448366
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64506374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985e13cf7b1d8354dc9c7667e5925ac3f77675b1215ef6c77b3de46929f4878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
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
$ docker pull docker@sha256:9f3ebcd963a0cfdf6d6a9d7ed0554e008343ca473b85d738527b763288ddb32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03` - linux; amd64

```console
$ docker pull docker@sha256:83a5911718a8e472a56f615f2939358508dfc6f6f0eaa460ef58460d7c18d723
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dab1a583eeee3300a1ff1fb14e75e0ab7cf2d4afb03c54801358fd3551e86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v6

```console
$ docker pull docker@sha256:d9e5bdce93b32511f9a1573e12db70984ece850504dd844af758a3cec1448366
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64506374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985e13cf7b1d8354dc9c7667e5925ac3f77675b1215ef6c77b3de46929f4878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
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
$ docker pull docker@sha256:9f3ebcd963a0cfdf6d6a9d7ed0554e008343ca473b85d738527b763288ddb32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.5` - linux; amd64

```console
$ docker pull docker@sha256:83a5911718a8e472a56f615f2939358508dfc6f6f0eaa460ef58460d7c18d723
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dab1a583eeee3300a1ff1fb14e75e0ab7cf2d4afb03c54801358fd3551e86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:d9e5bdce93b32511f9a1573e12db70984ece850504dd844af758a3cec1448366
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64506374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985e13cf7b1d8354dc9c7667e5925ac3f77675b1215ef6c77b3de46929f4878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
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
$ docker pull docker@sha256:59f32582b994492abb7f35bfa398b2cda9ea8f0386a5d7fbc44732ad4d8a411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d809dffd8e131480c43f8d527eed828f1d5a621f20b03a8467a22f655d9ad53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf5d4fc09c572da21c1fb641f77a4aa7879c7cbe5c4cc4469bcfe561b9182e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9c43fe631267f357df2985d3c3f7e70138c48b64cff93784c2eae59788d9990
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faead06f30f7cbd84302c7d35db261fc005a4c3afa745dca913999d73253e9f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:51:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:51:35 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:51:37 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:51:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 09 Jan 2020 23:49:49 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Thu, 09 Jan 2020 23:49:53 GMT
VOLUME [/var/lib/docker]
# Thu, 09 Jan 2020 23:49:55 GMT
EXPOSE 2375 2376
# Thu, 09 Jan 2020 23:49:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 09 Jan 2020 23:49:57 GMT
CMD []
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19801c3696a606cdfa10376aad90fb833530e5c00b7390044bb59716f5344d69`  
		Last Modified: Thu, 26 Dec 2019 21:53:04 GMT  
		Size: 3.2 MB (3212221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fae31fe824fbbe7c619386711de4a2ac0bb416850127be04b103f664bbd7cf`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b7d8d1ff5bbc65d1c330321373584880a3859b009a9e695d3399626867b558`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbba0a5ba1e4a6d0dbf73d1e7efc438ff713c8324e30b4b56338769a562321f`  
		Last Modified: Thu, 09 Jan 2020 23:50:24 GMT  
		Size: 2.5 KB (2533 bytes)  
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
$ docker pull docker@sha256:4c2b8e2c0035a9ee68cb20ad0716b20c92217a7b38df3de1e984f9d8176d1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c3ad4b82331f86d29bf56d2d4d42956bd120341b093289ab4649202b4ac1acae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97152021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c1cdede4fa811f0eb54ff4a93c2c7487ad0bb87e2457bea234918dcb42e15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
# Fri, 10 Jan 2020 00:21:43 GMT
RUN apk add --no-cache iproute2
# Fri, 10 Jan 2020 00:21:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Jan 2020 00:21:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Jan 2020 00:21:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 10 Jan 2020 00:21:47 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 10 Jan 2020 00:21:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 10 Jan 2020 00:21:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Jan 2020 00:21:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Jan 2020 00:21:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe8190e86c69446d5a5fec130d4018e323a517abb174b1fbdeb3f13328ed33`  
		Last Modified: Fri, 10 Jan 2020 00:22:22 GMT  
		Size: 796.0 KB (795976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d422b157253186347dbc9b498912cca79660336aeb3ff171e800ba3a716674e`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b29ef25925b69e6ed3fcd2e2c6d5a9d3081529d7c1658801a54ac4a89ff13`  
		Last Modified: Fri, 10 Jan 2020 00:22:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ceb8bbc160aaf5c9c2a10aa090a01cc0994009fd2fbda4670edb7da5d58f89`  
		Last Modified: Fri, 10 Jan 2020 00:22:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778579f341840460301b58bd23f124d3485c117b2dd9ef7fc6a399cec58cd517`  
		Last Modified: Fri, 10 Jan 2020 00:22:24 GMT  
		Size: 12.6 MB (12622925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8f8f70557c0b58c7c3d05ed9e1d5dada6e85950f5790eb1932b59ba50fd23`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.5-git`

```console
$ docker pull docker@sha256:8c1bf77657166db106a74f53162308d95a9b20944e9ad064c7c80f308a917aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.5-git` - linux; amd64

```console
$ docker pull docker@sha256:b6394c8848623428b143a1f4bac0a920bdb42f4f99c5b05087cf251507e65313
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77245713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad4a19dd9fb6fcbaa2a5f387a1e9845f7fbe38a034f7572e93f7b2d5b50786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:59 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b7903e0f55dbb52aa7db8437f06fb6ce233ee37f818c9df07d657ee5b00e7`  
		Last Modified: Thu, 26 Dec 2019 21:23:47 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.5-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:ba54eb58188a5d0d614a4d009ff88330d0bec0152dd140852542a9ce714ff424
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c1d9497f2cc9cc78ddfa01924c2cf965cc93c0198630ff6924fbeac741d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:52:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8691697b92d9e1787c16f801132a20df561fee79ee307c38ee605cb49586f3`  
		Last Modified: Thu, 26 Dec 2019 21:53:23 GMT  
		Size: 7.8 MB (7835199 bytes)  
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

## `docker:19.03-dind`

```console
$ docker pull docker@sha256:59f32582b994492abb7f35bfa398b2cda9ea8f0386a5d7fbc44732ad4d8a411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d809dffd8e131480c43f8d527eed828f1d5a621f20b03a8467a22f655d9ad53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf5d4fc09c572da21c1fb641f77a4aa7879c7cbe5c4cc4469bcfe561b9182e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9c43fe631267f357df2985d3c3f7e70138c48b64cff93784c2eae59788d9990
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faead06f30f7cbd84302c7d35db261fc005a4c3afa745dca913999d73253e9f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:51:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:51:35 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:51:37 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:51:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 09 Jan 2020 23:49:49 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Thu, 09 Jan 2020 23:49:53 GMT
VOLUME [/var/lib/docker]
# Thu, 09 Jan 2020 23:49:55 GMT
EXPOSE 2375 2376
# Thu, 09 Jan 2020 23:49:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 09 Jan 2020 23:49:57 GMT
CMD []
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19801c3696a606cdfa10376aad90fb833530e5c00b7390044bb59716f5344d69`  
		Last Modified: Thu, 26 Dec 2019 21:53:04 GMT  
		Size: 3.2 MB (3212221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fae31fe824fbbe7c619386711de4a2ac0bb416850127be04b103f664bbd7cf`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b7d8d1ff5bbc65d1c330321373584880a3859b009a9e695d3399626867b558`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbba0a5ba1e4a6d0dbf73d1e7efc438ff713c8324e30b4b56338769a562321f`  
		Last Modified: Thu, 09 Jan 2020 23:50:24 GMT  
		Size: 2.5 KB (2533 bytes)  
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
$ docker pull docker@sha256:4c2b8e2c0035a9ee68cb20ad0716b20c92217a7b38df3de1e984f9d8176d1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c3ad4b82331f86d29bf56d2d4d42956bd120341b093289ab4649202b4ac1acae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97152021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c1cdede4fa811f0eb54ff4a93c2c7487ad0bb87e2457bea234918dcb42e15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
# Fri, 10 Jan 2020 00:21:43 GMT
RUN apk add --no-cache iproute2
# Fri, 10 Jan 2020 00:21:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Jan 2020 00:21:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Jan 2020 00:21:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 10 Jan 2020 00:21:47 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 10 Jan 2020 00:21:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 10 Jan 2020 00:21:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Jan 2020 00:21:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Jan 2020 00:21:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe8190e86c69446d5a5fec130d4018e323a517abb174b1fbdeb3f13328ed33`  
		Last Modified: Fri, 10 Jan 2020 00:22:22 GMT  
		Size: 796.0 KB (795976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d422b157253186347dbc9b498912cca79660336aeb3ff171e800ba3a716674e`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b29ef25925b69e6ed3fcd2e2c6d5a9d3081529d7c1658801a54ac4a89ff13`  
		Last Modified: Fri, 10 Jan 2020 00:22:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ceb8bbc160aaf5c9c2a10aa090a01cc0994009fd2fbda4670edb7da5d58f89`  
		Last Modified: Fri, 10 Jan 2020 00:22:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778579f341840460301b58bd23f124d3485c117b2dd9ef7fc6a399cec58cd517`  
		Last Modified: Fri, 10 Jan 2020 00:22:24 GMT  
		Size: 12.6 MB (12622925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8f8f70557c0b58c7c3d05ed9e1d5dada6e85950f5790eb1932b59ba50fd23`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-git`

```console
$ docker pull docker@sha256:8c1bf77657166db106a74f53162308d95a9b20944e9ad064c7c80f308a917aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-git` - linux; amd64

```console
$ docker pull docker@sha256:b6394c8848623428b143a1f4bac0a920bdb42f4f99c5b05087cf251507e65313
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77245713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad4a19dd9fb6fcbaa2a5f387a1e9845f7fbe38a034f7572e93f7b2d5b50786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:59 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b7903e0f55dbb52aa7db8437f06fb6ce233ee37f818c9df07d657ee5b00e7`  
		Last Modified: Thu, 26 Dec 2019 21:23:47 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:ba54eb58188a5d0d614a4d009ff88330d0bec0152dd140852542a9ce714ff424
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c1d9497f2cc9cc78ddfa01924c2cf965cc93c0198630ff6924fbeac741d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:52:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8691697b92d9e1787c16f801132a20df561fee79ee307c38ee605cb49586f3`  
		Last Modified: Thu, 26 Dec 2019 21:53:23 GMT  
		Size: 7.8 MB (7835199 bytes)  
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

## `docker:19-dind`

```console
$ docker pull docker@sha256:59f32582b994492abb7f35bfa398b2cda9ea8f0386a5d7fbc44732ad4d8a411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d809dffd8e131480c43f8d527eed828f1d5a621f20b03a8467a22f655d9ad53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf5d4fc09c572da21c1fb641f77a4aa7879c7cbe5c4cc4469bcfe561b9182e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9c43fe631267f357df2985d3c3f7e70138c48b64cff93784c2eae59788d9990
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faead06f30f7cbd84302c7d35db261fc005a4c3afa745dca913999d73253e9f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:51:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:51:35 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:51:37 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:51:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 09 Jan 2020 23:49:49 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Thu, 09 Jan 2020 23:49:53 GMT
VOLUME [/var/lib/docker]
# Thu, 09 Jan 2020 23:49:55 GMT
EXPOSE 2375 2376
# Thu, 09 Jan 2020 23:49:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 09 Jan 2020 23:49:57 GMT
CMD []
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19801c3696a606cdfa10376aad90fb833530e5c00b7390044bb59716f5344d69`  
		Last Modified: Thu, 26 Dec 2019 21:53:04 GMT  
		Size: 3.2 MB (3212221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fae31fe824fbbe7c619386711de4a2ac0bb416850127be04b103f664bbd7cf`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b7d8d1ff5bbc65d1c330321373584880a3859b009a9e695d3399626867b558`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbba0a5ba1e4a6d0dbf73d1e7efc438ff713c8324e30b4b56338769a562321f`  
		Last Modified: Thu, 09 Jan 2020 23:50:24 GMT  
		Size: 2.5 KB (2533 bytes)  
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
$ docker pull docker@sha256:4c2b8e2c0035a9ee68cb20ad0716b20c92217a7b38df3de1e984f9d8176d1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c3ad4b82331f86d29bf56d2d4d42956bd120341b093289ab4649202b4ac1acae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97152021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c1cdede4fa811f0eb54ff4a93c2c7487ad0bb87e2457bea234918dcb42e15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
# Fri, 10 Jan 2020 00:21:43 GMT
RUN apk add --no-cache iproute2
# Fri, 10 Jan 2020 00:21:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Jan 2020 00:21:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Jan 2020 00:21:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 10 Jan 2020 00:21:47 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 10 Jan 2020 00:21:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 10 Jan 2020 00:21:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Jan 2020 00:21:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Jan 2020 00:21:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe8190e86c69446d5a5fec130d4018e323a517abb174b1fbdeb3f13328ed33`  
		Last Modified: Fri, 10 Jan 2020 00:22:22 GMT  
		Size: 796.0 KB (795976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d422b157253186347dbc9b498912cca79660336aeb3ff171e800ba3a716674e`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b29ef25925b69e6ed3fcd2e2c6d5a9d3081529d7c1658801a54ac4a89ff13`  
		Last Modified: Fri, 10 Jan 2020 00:22:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ceb8bbc160aaf5c9c2a10aa090a01cc0994009fd2fbda4670edb7da5d58f89`  
		Last Modified: Fri, 10 Jan 2020 00:22:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778579f341840460301b58bd23f124d3485c117b2dd9ef7fc6a399cec58cd517`  
		Last Modified: Fri, 10 Jan 2020 00:22:24 GMT  
		Size: 12.6 MB (12622925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8f8f70557c0b58c7c3d05ed9e1d5dada6e85950f5790eb1932b59ba50fd23`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-git`

```console
$ docker pull docker@sha256:8c1bf77657166db106a74f53162308d95a9b20944e9ad064c7c80f308a917aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-git` - linux; amd64

```console
$ docker pull docker@sha256:b6394c8848623428b143a1f4bac0a920bdb42f4f99c5b05087cf251507e65313
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77245713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad4a19dd9fb6fcbaa2a5f387a1e9845f7fbe38a034f7572e93f7b2d5b50786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:59 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b7903e0f55dbb52aa7db8437f06fb6ce233ee37f818c9df07d657ee5b00e7`  
		Last Modified: Thu, 26 Dec 2019 21:23:47 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:ba54eb58188a5d0d614a4d009ff88330d0bec0152dd140852542a9ce714ff424
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c1d9497f2cc9cc78ddfa01924c2cf965cc93c0198630ff6924fbeac741d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:52:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8691697b92d9e1787c16f801132a20df561fee79ee307c38ee605cb49586f3`  
		Last Modified: Thu, 26 Dec 2019 21:53:23 GMT  
		Size: 7.8 MB (7835199 bytes)  
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
$ docker pull docker@sha256:59f32582b994492abb7f35bfa398b2cda9ea8f0386a5d7fbc44732ad4d8a411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:2d809dffd8e131480c43f8d527eed828f1d5a621f20b03a8467a22f655d9ad53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf5d4fc09c572da21c1fb641f77a4aa7879c7cbe5c4cc4469bcfe561b9182e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9c43fe631267f357df2985d3c3f7e70138c48b64cff93784c2eae59788d9990
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faead06f30f7cbd84302c7d35db261fc005a4c3afa745dca913999d73253e9f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:51:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:51:35 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:51:37 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:51:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 09 Jan 2020 23:49:49 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Thu, 09 Jan 2020 23:49:53 GMT
VOLUME [/var/lib/docker]
# Thu, 09 Jan 2020 23:49:55 GMT
EXPOSE 2375 2376
# Thu, 09 Jan 2020 23:49:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 09 Jan 2020 23:49:57 GMT
CMD []
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19801c3696a606cdfa10376aad90fb833530e5c00b7390044bb59716f5344d69`  
		Last Modified: Thu, 26 Dec 2019 21:53:04 GMT  
		Size: 3.2 MB (3212221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fae31fe824fbbe7c619386711de4a2ac0bb416850127be04b103f664bbd7cf`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b7d8d1ff5bbc65d1c330321373584880a3859b009a9e695d3399626867b558`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbba0a5ba1e4a6d0dbf73d1e7efc438ff713c8324e30b4b56338769a562321f`  
		Last Modified: Thu, 09 Jan 2020 23:50:24 GMT  
		Size: 2.5 KB (2533 bytes)  
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
$ docker pull docker@sha256:4c2b8e2c0035a9ee68cb20ad0716b20c92217a7b38df3de1e984f9d8176d1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c3ad4b82331f86d29bf56d2d4d42956bd120341b093289ab4649202b4ac1acae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97152021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c1cdede4fa811f0eb54ff4a93c2c7487ad0bb87e2457bea234918dcb42e15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
# Fri, 10 Jan 2020 00:21:43 GMT
RUN apk add --no-cache iproute2
# Fri, 10 Jan 2020 00:21:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Jan 2020 00:21:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Jan 2020 00:21:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 10 Jan 2020 00:21:47 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 10 Jan 2020 00:21:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 10 Jan 2020 00:21:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Jan 2020 00:21:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Jan 2020 00:21:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe8190e86c69446d5a5fec130d4018e323a517abb174b1fbdeb3f13328ed33`  
		Last Modified: Fri, 10 Jan 2020 00:22:22 GMT  
		Size: 796.0 KB (795976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d422b157253186347dbc9b498912cca79660336aeb3ff171e800ba3a716674e`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b29ef25925b69e6ed3fcd2e2c6d5a9d3081529d7c1658801a54ac4a89ff13`  
		Last Modified: Fri, 10 Jan 2020 00:22:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ceb8bbc160aaf5c9c2a10aa090a01cc0994009fd2fbda4670edb7da5d58f89`  
		Last Modified: Fri, 10 Jan 2020 00:22:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778579f341840460301b58bd23f124d3485c117b2dd9ef7fc6a399cec58cd517`  
		Last Modified: Fri, 10 Jan 2020 00:22:24 GMT  
		Size: 12.6 MB (12622925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8f8f70557c0b58c7c3d05ed9e1d5dada6e85950f5790eb1932b59ba50fd23`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:8c1bf77657166db106a74f53162308d95a9b20944e9ad064c7c80f308a917aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:b6394c8848623428b143a1f4bac0a920bdb42f4f99c5b05087cf251507e65313
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77245713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad4a19dd9fb6fcbaa2a5f387a1e9845f7fbe38a034f7572e93f7b2d5b50786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:59 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b7903e0f55dbb52aa7db8437f06fb6ce233ee37f818c9df07d657ee5b00e7`  
		Last Modified: Thu, 26 Dec 2019 21:23:47 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:ba54eb58188a5d0d614a4d009ff88330d0bec0152dd140852542a9ce714ff424
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c1d9497f2cc9cc78ddfa01924c2cf965cc93c0198630ff6924fbeac741d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:52:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8691697b92d9e1787c16f801132a20df561fee79ee307c38ee605cb49586f3`  
		Last Modified: Thu, 26 Dec 2019 21:53:23 GMT  
		Size: 7.8 MB (7835199 bytes)  
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
$ docker pull docker@sha256:9f3ebcd963a0cfdf6d6a9d7ed0554e008343ca473b85d738527b763288ddb32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:83a5911718a8e472a56f615f2939358508dfc6f6f0eaa460ef58460d7c18d723
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dab1a583eeee3300a1ff1fb14e75e0ab7cf2d4afb03c54801358fd3551e86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:d9e5bdce93b32511f9a1573e12db70984ece850504dd844af758a3cec1448366
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64506374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985e13cf7b1d8354dc9c7667e5925ac3f77675b1215ef6c77b3de46929f4878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
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

## `docker:stable`

```console
$ docker pull docker@sha256:9f3ebcd963a0cfdf6d6a9d7ed0554e008343ca473b85d738527b763288ddb32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable` - linux; amd64

```console
$ docker pull docker@sha256:83a5911718a8e472a56f615f2939358508dfc6f6f0eaa460ef58460d7c18d723
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dab1a583eeee3300a1ff1fb14e75e0ab7cf2d4afb03c54801358fd3551e86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v6

```console
$ docker pull docker@sha256:d9e5bdce93b32511f9a1573e12db70984ece850504dd844af758a3cec1448366
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64506374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985e13cf7b1d8354dc9c7667e5925ac3f77675b1215ef6c77b3de46929f4878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
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
$ docker pull docker@sha256:59f32582b994492abb7f35bfa398b2cda9ea8f0386a5d7fbc44732ad4d8a411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d809dffd8e131480c43f8d527eed828f1d5a621f20b03a8467a22f655d9ad53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf5d4fc09c572da21c1fb641f77a4aa7879c7cbe5c4cc4469bcfe561b9182e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9c43fe631267f357df2985d3c3f7e70138c48b64cff93784c2eae59788d9990
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faead06f30f7cbd84302c7d35db261fc005a4c3afa745dca913999d73253e9f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:51:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:51:35 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:51:37 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:51:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 09 Jan 2020 23:49:49 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Thu, 09 Jan 2020 23:49:53 GMT
VOLUME [/var/lib/docker]
# Thu, 09 Jan 2020 23:49:55 GMT
EXPOSE 2375 2376
# Thu, 09 Jan 2020 23:49:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 09 Jan 2020 23:49:57 GMT
CMD []
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19801c3696a606cdfa10376aad90fb833530e5c00b7390044bb59716f5344d69`  
		Last Modified: Thu, 26 Dec 2019 21:53:04 GMT  
		Size: 3.2 MB (3212221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fae31fe824fbbe7c619386711de4a2ac0bb416850127be04b103f664bbd7cf`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b7d8d1ff5bbc65d1c330321373584880a3859b009a9e695d3399626867b558`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbba0a5ba1e4a6d0dbf73d1e7efc438ff713c8324e30b4b56338769a562321f`  
		Last Modified: Thu, 09 Jan 2020 23:50:24 GMT  
		Size: 2.5 KB (2533 bytes)  
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
$ docker pull docker@sha256:4c2b8e2c0035a9ee68cb20ad0716b20c92217a7b38df3de1e984f9d8176d1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:stable-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c3ad4b82331f86d29bf56d2d4d42956bd120341b093289ab4649202b4ac1acae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97152021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c1cdede4fa811f0eb54ff4a93c2c7487ad0bb87e2457bea234918dcb42e15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
# Fri, 10 Jan 2020 00:21:43 GMT
RUN apk add --no-cache iproute2
# Fri, 10 Jan 2020 00:21:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Jan 2020 00:21:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Jan 2020 00:21:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 10 Jan 2020 00:21:47 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 10 Jan 2020 00:21:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 10 Jan 2020 00:21:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Jan 2020 00:21:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Jan 2020 00:21:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe8190e86c69446d5a5fec130d4018e323a517abb174b1fbdeb3f13328ed33`  
		Last Modified: Fri, 10 Jan 2020 00:22:22 GMT  
		Size: 796.0 KB (795976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d422b157253186347dbc9b498912cca79660336aeb3ff171e800ba3a716674e`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b29ef25925b69e6ed3fcd2e2c6d5a9d3081529d7c1658801a54ac4a89ff13`  
		Last Modified: Fri, 10 Jan 2020 00:22:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ceb8bbc160aaf5c9c2a10aa090a01cc0994009fd2fbda4670edb7da5d58f89`  
		Last Modified: Fri, 10 Jan 2020 00:22:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778579f341840460301b58bd23f124d3485c117b2dd9ef7fc6a399cec58cd517`  
		Last Modified: Fri, 10 Jan 2020 00:22:24 GMT  
		Size: 12.6 MB (12622925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8f8f70557c0b58c7c3d05ed9e1d5dada6e85950f5790eb1932b59ba50fd23`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-git`

```console
$ docker pull docker@sha256:8c1bf77657166db106a74f53162308d95a9b20944e9ad064c7c80f308a917aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-git` - linux; amd64

```console
$ docker pull docker@sha256:b6394c8848623428b143a1f4bac0a920bdb42f4f99c5b05087cf251507e65313
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77245713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad4a19dd9fb6fcbaa2a5f387a1e9845f7fbe38a034f7572e93f7b2d5b50786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:59 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b7903e0f55dbb52aa7db8437f06fb6ce233ee37f818c9df07d657ee5b00e7`  
		Last Modified: Thu, 26 Dec 2019 21:23:47 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:ba54eb58188a5d0d614a4d009ff88330d0bec0152dd140852542a9ce714ff424
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c1d9497f2cc9cc78ddfa01924c2cf965cc93c0198630ff6924fbeac741d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:52:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8691697b92d9e1787c16f801132a20df561fee79ee307c38ee605cb49586f3`  
		Last Modified: Thu, 26 Dec 2019 21:53:23 GMT  
		Size: 7.8 MB (7835199 bytes)  
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
$ docker pull docker@sha256:9f3ebcd963a0cfdf6d6a9d7ed0554e008343ca473b85d738527b763288ddb32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test` - linux; amd64

```console
$ docker pull docker@sha256:83a5911718a8e472a56f615f2939358508dfc6f6f0eaa460ef58460d7c18d723
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dab1a583eeee3300a1ff1fb14e75e0ab7cf2d4afb03c54801358fd3551e86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm variant v6

```console
$ docker pull docker@sha256:d9e5bdce93b32511f9a1573e12db70984ece850504dd844af758a3cec1448366
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64506374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985e13cf7b1d8354dc9c7667e5925ac3f77675b1215ef6c77b3de46929f4878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm variant v7

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

### `docker:test` - linux; arm64 variant v8

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

## `docker:test-dind`

```console
$ docker pull docker@sha256:59f32582b994492abb7f35bfa398b2cda9ea8f0386a5d7fbc44732ad4d8a411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d809dffd8e131480c43f8d527eed828f1d5a621f20b03a8467a22f655d9ad53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf5d4fc09c572da21c1fb641f77a4aa7879c7cbe5c4cc4469bcfe561b9182e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9c43fe631267f357df2985d3c3f7e70138c48b64cff93784c2eae59788d9990
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faead06f30f7cbd84302c7d35db261fc005a4c3afa745dca913999d73253e9f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:51:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:51:35 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:51:37 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:51:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 09 Jan 2020 23:49:49 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Thu, 09 Jan 2020 23:49:53 GMT
VOLUME [/var/lib/docker]
# Thu, 09 Jan 2020 23:49:55 GMT
EXPOSE 2375 2376
# Thu, 09 Jan 2020 23:49:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 09 Jan 2020 23:49:57 GMT
CMD []
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19801c3696a606cdfa10376aad90fb833530e5c00b7390044bb59716f5344d69`  
		Last Modified: Thu, 26 Dec 2019 21:53:04 GMT  
		Size: 3.2 MB (3212221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fae31fe824fbbe7c619386711de4a2ac0bb416850127be04b103f664bbd7cf`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b7d8d1ff5bbc65d1c330321373584880a3859b009a9e695d3399626867b558`  
		Last Modified: Thu, 26 Dec 2019 21:53:03 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbba0a5ba1e4a6d0dbf73d1e7efc438ff713c8324e30b4b56338769a562321f`  
		Last Modified: Thu, 09 Jan 2020 23:50:24 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v7

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

### `docker:test-dind` - linux; arm64 variant v8

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

## `docker:test-dind-rootless`

```console
$ docker pull docker@sha256:4c2b8e2c0035a9ee68cb20ad0716b20c92217a7b38df3de1e984f9d8176d1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:test-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c3ad4b82331f86d29bf56d2d4d42956bd120341b093289ab4649202b4ac1acae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97152021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8c1cdede4fa811f0eb54ff4a93c2c7487ad0bb87e2457bea234918dcb42e15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Jan 2020 00:21:38 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 10 Jan 2020 00:21:38 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Jan 2020 00:21:38 GMT
EXPOSE 2375 2376
# Fri, 10 Jan 2020 00:21:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Jan 2020 00:21:38 GMT
CMD []
# Fri, 10 Jan 2020 00:21:43 GMT
RUN apk add --no-cache iproute2
# Fri, 10 Jan 2020 00:21:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Jan 2020 00:21:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Jan 2020 00:21:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 10 Jan 2020 00:21:47 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 10 Jan 2020 00:21:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 10 Jan 2020 00:21:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Jan 2020 00:21:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Jan 2020 00:21:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5b3aaea0ce2c12ecb64eb64832d276a7497a3010077a80e92d08eb0f44f7a`  
		Last Modified: Fri, 10 Jan 2020 00:22:14 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe8190e86c69446d5a5fec130d4018e323a517abb174b1fbdeb3f13328ed33`  
		Last Modified: Fri, 10 Jan 2020 00:22:22 GMT  
		Size: 796.0 KB (795976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d422b157253186347dbc9b498912cca79660336aeb3ff171e800ba3a716674e`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b29ef25925b69e6ed3fcd2e2c6d5a9d3081529d7c1658801a54ac4a89ff13`  
		Last Modified: Fri, 10 Jan 2020 00:22:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ceb8bbc160aaf5c9c2a10aa090a01cc0994009fd2fbda4670edb7da5d58f89`  
		Last Modified: Fri, 10 Jan 2020 00:22:23 GMT  
		Size: 9.1 MB (9109459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778579f341840460301b58bd23f124d3485c117b2dd9ef7fc6a399cec58cd517`  
		Last Modified: Fri, 10 Jan 2020 00:22:24 GMT  
		Size: 12.6 MB (12622925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8f8f70557c0b58c7c3d05ed9e1d5dada6e85950f5790eb1932b59ba50fd23`  
		Last Modified: Fri, 10 Jan 2020 00:22:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-git`

```console
$ docker pull docker@sha256:8c1bf77657166db106a74f53162308d95a9b20944e9ad064c7c80f308a917aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-git` - linux; amd64

```console
$ docker pull docker@sha256:b6394c8848623428b143a1f4bac0a920bdb42f4f99c5b05087cf251507e65313
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77245713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad4a19dd9fb6fcbaa2a5f387a1e9845f7fbe38a034f7572e93f7b2d5b50786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:59 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b7903e0f55dbb52aa7db8437f06fb6ce233ee37f818c9df07d657ee5b00e7`  
		Last Modified: Thu, 26 Dec 2019 21:23:47 GMT  
		Size: 8.2 MB (8213895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:ba54eb58188a5d0d614a4d009ff88330d0bec0152dd140852542a9ce714ff424
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72341573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c1d9497f2cc9cc78ddfa01924c2cf965cc93c0198630ff6924fbeac741d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:50:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:50:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:50:52 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:50:53 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:51:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:51:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:51:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:51:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:51:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:51:16 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:52:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478492ea0683b34ae904eef577598b09ce1dbe4230af7a3920720bb816e95191`  
		Last Modified: Thu, 26 Dec 2019 21:52:34 GMT  
		Size: 2.4 MB (2355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3af0915702a94dc803895239d700514ff4b25b946a55c5feaa45887c6dd649`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9411ea300b6cb0357017a7622e46a795c7a7acd744893d1157858f9be65f7`  
		Last Modified: Thu, 26 Dec 2019 21:52:48 GMT  
		Size: 59.5 MB (59537091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f1ebb3f7fc87e3bd0fb06d4453594906d54e705a7a7e438259429633cca29`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ae19a6988bc39dbec026bcd5c3533ea6c1f878e700d24b87fac38624d4cb4`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84874978fd32476c30a94a54a06631d103a9144642b463482f821b4176dc03ff`  
		Last Modified: Thu, 26 Dec 2019 21:52:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8691697b92d9e1787c16f801132a20df561fee79ee307c38ee605cb49586f3`  
		Last Modified: Thu, 26 Dec 2019 21:53:23 GMT  
		Size: 7.8 MB (7835199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v7

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

### `docker:test-git` - linux; arm64 variant v8

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

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

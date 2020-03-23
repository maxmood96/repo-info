<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:19`](#docker19)
-	[`docker:19.03`](#docker1903)
-	[`docker:19.03.8`](#docker19038)
-	[`docker:19.03.8-dind`](#docker19038-dind)
-	[`docker:19.03.8-dind-rootless`](#docker19038-dind-rootless)
-	[`docker:19.03.8-git`](#docker19038-git)
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
$ docker pull docker@sha256:afea2876df8334e5430d2427cfd37b39be2ee497db76d3651b2b14d97de4b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19` - linux; amd64

```console
$ docker pull docker@sha256:aaead6545f3f63850ba8cbd1cf9cbe85e0cc9a512ec4d23060b0b69c5d72680e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2e482e9de9ca3939dce4c90810c89fa7e7450f774590967c2908cba857ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v6

```console
$ docker pull docker@sha256:f5e47dbe2b0e0c18a594b8f963bee76a360d900cc8ba83a6e00afecb2e4d4c02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679551e5cdc51461a4b78e1f8ce583384562f2acbbfd7655012853993740f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm variant v7

```console
$ docker pull docker@sha256:9578d4c298343d2083bf58baafac2923eb9ceb109ab0b879ee502b380cb48384
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26135427427a7f96bf806d0b05d2c5d8145d2ee1fa8a74cf95f520b72060624a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8050f22a8d227118300d650bde0c3a1d418b98ac72962d933419f878384bc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e59ae775d55303c7e29acd62f3a1764673c91d4436b4232d427a38d5cf6277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03`

```console
$ docker pull docker@sha256:afea2876df8334e5430d2427cfd37b39be2ee497db76d3651b2b14d97de4b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03` - linux; amd64

```console
$ docker pull docker@sha256:aaead6545f3f63850ba8cbd1cf9cbe85e0cc9a512ec4d23060b0b69c5d72680e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2e482e9de9ca3939dce4c90810c89fa7e7450f774590967c2908cba857ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v6

```console
$ docker pull docker@sha256:f5e47dbe2b0e0c18a594b8f963bee76a360d900cc8ba83a6e00afecb2e4d4c02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679551e5cdc51461a4b78e1f8ce583384562f2acbbfd7655012853993740f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm variant v7

```console
$ docker pull docker@sha256:9578d4c298343d2083bf58baafac2923eb9ceb109ab0b879ee502b380cb48384
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26135427427a7f96bf806d0b05d2c5d8145d2ee1fa8a74cf95f520b72060624a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8050f22a8d227118300d650bde0c3a1d418b98ac72962d933419f878384bc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e59ae775d55303c7e29acd62f3a1764673c91d4436b4232d427a38d5cf6277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8`

```console
$ docker pull docker@sha256:afea2876df8334e5430d2427cfd37b39be2ee497db76d3651b2b14d97de4b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.8` - linux; amd64

```console
$ docker pull docker@sha256:aaead6545f3f63850ba8cbd1cf9cbe85e0cc9a512ec4d23060b0b69c5d72680e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2e482e9de9ca3939dce4c90810c89fa7e7450f774590967c2908cba857ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8` - linux; arm variant v6

```console
$ docker pull docker@sha256:f5e47dbe2b0e0c18a594b8f963bee76a360d900cc8ba83a6e00afecb2e4d4c02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679551e5cdc51461a4b78e1f8ce583384562f2acbbfd7655012853993740f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8` - linux; arm variant v7

```console
$ docker pull docker@sha256:9578d4c298343d2083bf58baafac2923eb9ceb109ab0b879ee502b380cb48384
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26135427427a7f96bf806d0b05d2c5d8145d2ee1fa8a74cf95f520b72060624a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8050f22a8d227118300d650bde0c3a1d418b98ac72962d933419f878384bc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e59ae775d55303c7e29acd62f3a1764673c91d4436b4232d427a38d5cf6277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8-dind`

```console
$ docker pull docker@sha256:ba51388db2907f0f0d33b365f039f89b48bfe9e3a408c2211addd5357268f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.8-dind` - linux; amd64

```console
$ docker pull docker@sha256:ad5b5195369a35265a33701ebea33065fa4c444de99bddece07637cff061afd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74564667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e51fd179fb849f4ec6faee318101d32830103f5615215716bd686c56afaea1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c9557e5f2b9b8fa553aa6f907a6d12f2217591cef74462b52e2e9d6bbb23ace3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a39444acd2e083ced4230738bb4707c7c3b7f7d6726e313d160b6f6543283d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:05:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:05:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:05:55 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:05:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:05:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:58 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:05:59 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:06:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:06:00 GMT
CMD []
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7ba7497a4c01d268a06a05014b168ac1cb74413c6e0ae710ad3469530c89c`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 3.2 MB (3160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5904ee04ec79e4943102f425fc2f4d79499f8ec03fdb360017c7cfdba8d05be`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe794901e085309747f4f7be9ecbc65c7c1b6f9e8ea863309588d3593115139`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c876279fc6bc524f2a67d73903959bf8d6b566159fbc4375d46de90534bf892`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29d8e06c8142bacc57bcf2bc3a1699f714e8896eab373c818af9ed53c2f65377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67002022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fc21e7e3d4d6ca3ac07203e6db78cdec4c686619b7f96ace77896164ea007`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:16:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:16:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:16:48 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:16:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:16:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:17:03 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:17:07 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:17:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:17:20 GMT
CMD []
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe56a4b6c1f198928eca7534f4247591aa211cd3d569187330b5c19783d171`  
		Last Modified: Mon, 23 Mar 2020 22:18:49 GMT  
		Size: 2.8 MB (2824370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932c1314c55e1e27c3d804ffffcce7b03a320adeebf297080709ea75795aa70`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62999c7314ddbf68e6aab71c9d95eb4ad7656b186eb79e2b5c966781e9521b3e`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 751.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52386e4e869ce89244a2e79701b0d07d531edc12fead5e7659c2ec2c9d63dc`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79b64df37e8a4dd5caa6f4425e92968af863d8aed47cf92045a660926ae4530c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01edd0e422bca03945f4e087ab929db62bc948338682b5a4d8f85d214c301b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:02:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:02:20 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:02:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:02:22 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:22 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:02:23 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:02:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:24 GMT
CMD []
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efd0796f1d1e7e4bce8afa5e864062d575e574570cbdb39b5deab65202fb353`  
		Last Modified: Mon, 23 Mar 2020 22:03:21 GMT  
		Size: 5.5 MB (5544906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ceab62b056e368760dc0a031792b7745ae4966225a33ddc1cb15cb47550ad`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9000337c3a99f635eafb642bd725f4542ee547c959d7e0021b352c6d716fad8`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c2f52ca3c7d3802e22e5a5983407c6e6b79cba6d7dd481854626f0d707286`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8-dind-rootless`

```console
$ docker pull docker@sha256:5d1da82e27e5bee17e5b45f6eeb635392ac9a080e0ffb88051891a507614ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03.8-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9558020a63545edf61ceb921d1a712558df7bda3b970526191a367331eb66921
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97568213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdb45ee65acf6c0bce72f059897f9b17f7f7e4a4574ffe26994ba5e7c054c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
# Mon, 23 Mar 2020 21:37:23 GMT
RUN apk add --no-cache iproute2
# Mon, 23 Mar 2020 21:37:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 23 Mar 2020 21:37:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 23 Mar 2020 21:37:27 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 23 Mar 2020 21:37:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 23 Mar 2020 21:37:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 23 Mar 2020 21:37:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Mar 2020 21:37:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a271affe02af7f7c17c21afea5a80c7a7beef90fd35d3d1b777a546efbc09`  
		Last Modified: Mon, 23 Mar 2020 21:38:30 GMT  
		Size: 737.8 KB (737788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e335660b237b8ba9e44067b870612e2d7bc537c0c44cb76817e3b1553ca143`  
		Last Modified: Mon, 23 Mar 2020 21:38:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bed69641936f2f620cfc29b51dbb90f205539edb8e12f7c764a9fcaa09025f`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993191c7a55ab3c67f49c847e77fc68b47ebd297d0df6cbe6a7cbcd9e1e290b7`  
		Last Modified: Mon, 23 Mar 2020 21:38:32 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e354682f72a669ca6ab57fdf4ebfbc2e813048e00372ae1cb173b996989e43`  
		Last Modified: Mon, 23 Mar 2020 21:38:31 GMT  
		Size: 13.2 MB (13154699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ff660f1e572dfe9c3db055dc0a27bd6976ebaa7bf27719af582483680ac309`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03.8-git`

```console
$ docker pull docker@sha256:c061e3894336ba0dbf26144b7d816f59cedb2d0304fb11cc8bab21f9fabcf4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03.8-git` - linux; amd64

```console
$ docker pull docker@sha256:b13a275725f070a0bfcaf68ce6474ad47008ca29ff3d1de21836d342967e37bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86091642623aa4d51ccc77f196b7640513334cc07c79636d2c3648defb3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:47 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145837c41213d104c08dc578bbdcab4a9f23a403ff9bdd5285b54e339568287e`  
		Last Modified: Mon, 23 Mar 2020 21:38:40 GMT  
		Size: 8.2 MB (8158656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:7eb1117ebd89423822f0880254dbf87ee699d9a8efe0b07d82d95e3a372b99d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72258644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08be4718e8abfbb5d121202beb674a899eac334a25a973d73dbf3baf362513b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:06:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8d8b3216f7fcba0890fbe2e2c803188979a28a9cb7b8bc4550ff9bb1a9343`  
		Last Modified: Mon, 23 Mar 2020 22:07:17 GMT  
		Size: 7.8 MB (7782806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:dbe9d61f34600e33e6bc49fad0c6ad63c770ea097b046378517faaf82d83cf85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754651b3b148fa5ef97050227c8ec8b6fa3f23f75fbe4467e0a0e06171f2c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:17:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6d158b95a40b14d93047b67c03bee7d0d66d9dff39b5016d34f3a9fa4c01`  
		Last Modified: Mon, 23 Mar 2020 22:19:07 GMT  
		Size: 7.0 MB (7012560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03.8-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c84b97ad756af72337727cb4e0b1269316b217dfeb27e5c6eeabaec4ad28a45a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70481944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7335b0dfaf0da2807689d7667205c01f848415edeb7fe5f8d793ba1fd04052e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:32 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd6cbbd7d27a1cb69e5062a96cd9f22877ad55d251d5ff5ce84a8480be0ea3`  
		Last Modified: Mon, 23 Mar 2020 22:03:34 GMT  
		Size: 8.4 MB (8354040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind`

```console
$ docker pull docker@sha256:ba51388db2907f0f0d33b365f039f89b48bfe9e3a408c2211addd5357268f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-dind` - linux; amd64

```console
$ docker pull docker@sha256:ad5b5195369a35265a33701ebea33065fa4c444de99bddece07637cff061afd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74564667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e51fd179fb849f4ec6faee318101d32830103f5615215716bd686c56afaea1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c9557e5f2b9b8fa553aa6f907a6d12f2217591cef74462b52e2e9d6bbb23ace3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a39444acd2e083ced4230738bb4707c7c3b7f7d6726e313d160b6f6543283d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:05:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:05:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:05:55 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:05:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:05:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:58 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:05:59 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:06:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:06:00 GMT
CMD []
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7ba7497a4c01d268a06a05014b168ac1cb74413c6e0ae710ad3469530c89c`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 3.2 MB (3160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5904ee04ec79e4943102f425fc2f4d79499f8ec03fdb360017c7cfdba8d05be`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe794901e085309747f4f7be9ecbc65c7c1b6f9e8ea863309588d3593115139`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c876279fc6bc524f2a67d73903959bf8d6b566159fbc4375d46de90534bf892`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29d8e06c8142bacc57bcf2bc3a1699f714e8896eab373c818af9ed53c2f65377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67002022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fc21e7e3d4d6ca3ac07203e6db78cdec4c686619b7f96ace77896164ea007`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:16:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:16:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:16:48 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:16:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:16:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:17:03 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:17:07 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:17:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:17:20 GMT
CMD []
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe56a4b6c1f198928eca7534f4247591aa211cd3d569187330b5c19783d171`  
		Last Modified: Mon, 23 Mar 2020 22:18:49 GMT  
		Size: 2.8 MB (2824370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932c1314c55e1e27c3d804ffffcce7b03a320adeebf297080709ea75795aa70`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62999c7314ddbf68e6aab71c9d95eb4ad7656b186eb79e2b5c966781e9521b3e`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 751.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52386e4e869ce89244a2e79701b0d07d531edc12fead5e7659c2ec2c9d63dc`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79b64df37e8a4dd5caa6f4425e92968af863d8aed47cf92045a660926ae4530c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01edd0e422bca03945f4e087ab929db62bc948338682b5a4d8f85d214c301b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:02:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:02:20 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:02:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:02:22 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:22 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:02:23 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:02:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:24 GMT
CMD []
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efd0796f1d1e7e4bce8afa5e864062d575e574570cbdb39b5deab65202fb353`  
		Last Modified: Mon, 23 Mar 2020 22:03:21 GMT  
		Size: 5.5 MB (5544906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ceab62b056e368760dc0a031792b7745ae4966225a33ddc1cb15cb47550ad`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9000337c3a99f635eafb642bd725f4542ee547c959d7e0021b352c6d716fad8`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c2f52ca3c7d3802e22e5a5983407c6e6b79cba6d7dd481854626f0d707286`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-dind-rootless`

```console
$ docker pull docker@sha256:5d1da82e27e5bee17e5b45f6eeb635392ac9a080e0ffb88051891a507614ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19.03-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9558020a63545edf61ceb921d1a712558df7bda3b970526191a367331eb66921
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97568213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdb45ee65acf6c0bce72f059897f9b17f7f7e4a4574ffe26994ba5e7c054c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
# Mon, 23 Mar 2020 21:37:23 GMT
RUN apk add --no-cache iproute2
# Mon, 23 Mar 2020 21:37:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 23 Mar 2020 21:37:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 23 Mar 2020 21:37:27 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 23 Mar 2020 21:37:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 23 Mar 2020 21:37:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 23 Mar 2020 21:37:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Mar 2020 21:37:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a271affe02af7f7c17c21afea5a80c7a7beef90fd35d3d1b777a546efbc09`  
		Last Modified: Mon, 23 Mar 2020 21:38:30 GMT  
		Size: 737.8 KB (737788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e335660b237b8ba9e44067b870612e2d7bc537c0c44cb76817e3b1553ca143`  
		Last Modified: Mon, 23 Mar 2020 21:38:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bed69641936f2f620cfc29b51dbb90f205539edb8e12f7c764a9fcaa09025f`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993191c7a55ab3c67f49c847e77fc68b47ebd297d0df6cbe6a7cbcd9e1e290b7`  
		Last Modified: Mon, 23 Mar 2020 21:38:32 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e354682f72a669ca6ab57fdf4ebfbc2e813048e00372ae1cb173b996989e43`  
		Last Modified: Mon, 23 Mar 2020 21:38:31 GMT  
		Size: 13.2 MB (13154699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ff660f1e572dfe9c3db055dc0a27bd6976ebaa7bf27719af582483680ac309`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19.03-git`

```console
$ docker pull docker@sha256:c061e3894336ba0dbf26144b7d816f59cedb2d0304fb11cc8bab21f9fabcf4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19.03-git` - linux; amd64

```console
$ docker pull docker@sha256:b13a275725f070a0bfcaf68ce6474ad47008ca29ff3d1de21836d342967e37bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86091642623aa4d51ccc77f196b7640513334cc07c79636d2c3648defb3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:47 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145837c41213d104c08dc578bbdcab4a9f23a403ff9bdd5285b54e339568287e`  
		Last Modified: Mon, 23 Mar 2020 21:38:40 GMT  
		Size: 8.2 MB (8158656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:7eb1117ebd89423822f0880254dbf87ee699d9a8efe0b07d82d95e3a372b99d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72258644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08be4718e8abfbb5d121202beb674a899eac334a25a973d73dbf3baf362513b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:06:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8d8b3216f7fcba0890fbe2e2c803188979a28a9cb7b8bc4550ff9bb1a9343`  
		Last Modified: Mon, 23 Mar 2020 22:07:17 GMT  
		Size: 7.8 MB (7782806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:dbe9d61f34600e33e6bc49fad0c6ad63c770ea097b046378517faaf82d83cf85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754651b3b148fa5ef97050227c8ec8b6fa3f23f75fbe4467e0a0e06171f2c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:17:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6d158b95a40b14d93047b67c03bee7d0d66d9dff39b5016d34f3a9fa4c01`  
		Last Modified: Mon, 23 Mar 2020 22:19:07 GMT  
		Size: 7.0 MB (7012560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19.03-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c84b97ad756af72337727cb4e0b1269316b217dfeb27e5c6eeabaec4ad28a45a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70481944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7335b0dfaf0da2807689d7667205c01f848415edeb7fe5f8d793ba1fd04052e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:32 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd6cbbd7d27a1cb69e5062a96cd9f22877ad55d251d5ff5ce84a8480be0ea3`  
		Last Modified: Mon, 23 Mar 2020 22:03:34 GMT  
		Size: 8.4 MB (8354040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind`

```console
$ docker pull docker@sha256:ba51388db2907f0f0d33b365f039f89b48bfe9e3a408c2211addd5357268f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-dind` - linux; amd64

```console
$ docker pull docker@sha256:ad5b5195369a35265a33701ebea33065fa4c444de99bddece07637cff061afd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74564667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e51fd179fb849f4ec6faee318101d32830103f5615215716bd686c56afaea1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c9557e5f2b9b8fa553aa6f907a6d12f2217591cef74462b52e2e9d6bbb23ace3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a39444acd2e083ced4230738bb4707c7c3b7f7d6726e313d160b6f6543283d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:05:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:05:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:05:55 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:05:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:05:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:58 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:05:59 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:06:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:06:00 GMT
CMD []
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7ba7497a4c01d268a06a05014b168ac1cb74413c6e0ae710ad3469530c89c`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 3.2 MB (3160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5904ee04ec79e4943102f425fc2f4d79499f8ec03fdb360017c7cfdba8d05be`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe794901e085309747f4f7be9ecbc65c7c1b6f9e8ea863309588d3593115139`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c876279fc6bc524f2a67d73903959bf8d6b566159fbc4375d46de90534bf892`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29d8e06c8142bacc57bcf2bc3a1699f714e8896eab373c818af9ed53c2f65377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67002022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fc21e7e3d4d6ca3ac07203e6db78cdec4c686619b7f96ace77896164ea007`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:16:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:16:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:16:48 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:16:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:16:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:17:03 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:17:07 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:17:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:17:20 GMT
CMD []
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe56a4b6c1f198928eca7534f4247591aa211cd3d569187330b5c19783d171`  
		Last Modified: Mon, 23 Mar 2020 22:18:49 GMT  
		Size: 2.8 MB (2824370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932c1314c55e1e27c3d804ffffcce7b03a320adeebf297080709ea75795aa70`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62999c7314ddbf68e6aab71c9d95eb4ad7656b186eb79e2b5c966781e9521b3e`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 751.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52386e4e869ce89244a2e79701b0d07d531edc12fead5e7659c2ec2c9d63dc`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79b64df37e8a4dd5caa6f4425e92968af863d8aed47cf92045a660926ae4530c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01edd0e422bca03945f4e087ab929db62bc948338682b5a4d8f85d214c301b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:02:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:02:20 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:02:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:02:22 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:22 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:02:23 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:02:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:24 GMT
CMD []
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efd0796f1d1e7e4bce8afa5e864062d575e574570cbdb39b5deab65202fb353`  
		Last Modified: Mon, 23 Mar 2020 22:03:21 GMT  
		Size: 5.5 MB (5544906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ceab62b056e368760dc0a031792b7745ae4966225a33ddc1cb15cb47550ad`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9000337c3a99f635eafb642bd725f4542ee547c959d7e0021b352c6d716fad8`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c2f52ca3c7d3802e22e5a5983407c6e6b79cba6d7dd481854626f0d707286`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:5d1da82e27e5bee17e5b45f6eeb635392ac9a080e0ffb88051891a507614ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9558020a63545edf61ceb921d1a712558df7bda3b970526191a367331eb66921
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97568213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdb45ee65acf6c0bce72f059897f9b17f7f7e4a4574ffe26994ba5e7c054c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
# Mon, 23 Mar 2020 21:37:23 GMT
RUN apk add --no-cache iproute2
# Mon, 23 Mar 2020 21:37:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 23 Mar 2020 21:37:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 23 Mar 2020 21:37:27 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 23 Mar 2020 21:37:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 23 Mar 2020 21:37:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 23 Mar 2020 21:37:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Mar 2020 21:37:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a271affe02af7f7c17c21afea5a80c7a7beef90fd35d3d1b777a546efbc09`  
		Last Modified: Mon, 23 Mar 2020 21:38:30 GMT  
		Size: 737.8 KB (737788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e335660b237b8ba9e44067b870612e2d7bc537c0c44cb76817e3b1553ca143`  
		Last Modified: Mon, 23 Mar 2020 21:38:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bed69641936f2f620cfc29b51dbb90f205539edb8e12f7c764a9fcaa09025f`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993191c7a55ab3c67f49c847e77fc68b47ebd297d0df6cbe6a7cbcd9e1e290b7`  
		Last Modified: Mon, 23 Mar 2020 21:38:32 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e354682f72a669ca6ab57fdf4ebfbc2e813048e00372ae1cb173b996989e43`  
		Last Modified: Mon, 23 Mar 2020 21:38:31 GMT  
		Size: 13.2 MB (13154699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ff660f1e572dfe9c3db055dc0a27bd6976ebaa7bf27719af582483680ac309`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:19-git`

```console
$ docker pull docker@sha256:c061e3894336ba0dbf26144b7d816f59cedb2d0304fb11cc8bab21f9fabcf4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:19-git` - linux; amd64

```console
$ docker pull docker@sha256:b13a275725f070a0bfcaf68ce6474ad47008ca29ff3d1de21836d342967e37bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86091642623aa4d51ccc77f196b7640513334cc07c79636d2c3648defb3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:47 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145837c41213d104c08dc578bbdcab4a9f23a403ff9bdd5285b54e339568287e`  
		Last Modified: Mon, 23 Mar 2020 21:38:40 GMT  
		Size: 8.2 MB (8158656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:7eb1117ebd89423822f0880254dbf87ee699d9a8efe0b07d82d95e3a372b99d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72258644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08be4718e8abfbb5d121202beb674a899eac334a25a973d73dbf3baf362513b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:06:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8d8b3216f7fcba0890fbe2e2c803188979a28a9cb7b8bc4550ff9bb1a9343`  
		Last Modified: Mon, 23 Mar 2020 22:07:17 GMT  
		Size: 7.8 MB (7782806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:dbe9d61f34600e33e6bc49fad0c6ad63c770ea097b046378517faaf82d83cf85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754651b3b148fa5ef97050227c8ec8b6fa3f23f75fbe4467e0a0e06171f2c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:17:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6d158b95a40b14d93047b67c03bee7d0d66d9dff39b5016d34f3a9fa4c01`  
		Last Modified: Mon, 23 Mar 2020 22:19:07 GMT  
		Size: 7.0 MB (7012560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:19-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c84b97ad756af72337727cb4e0b1269316b217dfeb27e5c6eeabaec4ad28a45a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70481944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7335b0dfaf0da2807689d7667205c01f848415edeb7fe5f8d793ba1fd04052e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:32 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd6cbbd7d27a1cb69e5062a96cd9f22877ad55d251d5ff5ce84a8480be0ea3`  
		Last Modified: Mon, 23 Mar 2020 22:03:34 GMT  
		Size: 8.4 MB (8354040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:ba51388db2907f0f0d33b365f039f89b48bfe9e3a408c2211addd5357268f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:ad5b5195369a35265a33701ebea33065fa4c444de99bddece07637cff061afd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74564667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e51fd179fb849f4ec6faee318101d32830103f5615215716bd686c56afaea1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c9557e5f2b9b8fa553aa6f907a6d12f2217591cef74462b52e2e9d6bbb23ace3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a39444acd2e083ced4230738bb4707c7c3b7f7d6726e313d160b6f6543283d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:05:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:05:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:05:55 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:05:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:05:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:58 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:05:59 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:06:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:06:00 GMT
CMD []
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7ba7497a4c01d268a06a05014b168ac1cb74413c6e0ae710ad3469530c89c`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 3.2 MB (3160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5904ee04ec79e4943102f425fc2f4d79499f8ec03fdb360017c7cfdba8d05be`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe794901e085309747f4f7be9ecbc65c7c1b6f9e8ea863309588d3593115139`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c876279fc6bc524f2a67d73903959bf8d6b566159fbc4375d46de90534bf892`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29d8e06c8142bacc57bcf2bc3a1699f714e8896eab373c818af9ed53c2f65377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67002022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fc21e7e3d4d6ca3ac07203e6db78cdec4c686619b7f96ace77896164ea007`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:16:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:16:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:16:48 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:16:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:16:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:17:03 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:17:07 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:17:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:17:20 GMT
CMD []
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe56a4b6c1f198928eca7534f4247591aa211cd3d569187330b5c19783d171`  
		Last Modified: Mon, 23 Mar 2020 22:18:49 GMT  
		Size: 2.8 MB (2824370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932c1314c55e1e27c3d804ffffcce7b03a320adeebf297080709ea75795aa70`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62999c7314ddbf68e6aab71c9d95eb4ad7656b186eb79e2b5c966781e9521b3e`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 751.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52386e4e869ce89244a2e79701b0d07d531edc12fead5e7659c2ec2c9d63dc`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79b64df37e8a4dd5caa6f4425e92968af863d8aed47cf92045a660926ae4530c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01edd0e422bca03945f4e087ab929db62bc948338682b5a4d8f85d214c301b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:02:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:02:20 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:02:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:02:22 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:22 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:02:23 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:02:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:24 GMT
CMD []
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efd0796f1d1e7e4bce8afa5e864062d575e574570cbdb39b5deab65202fb353`  
		Last Modified: Mon, 23 Mar 2020 22:03:21 GMT  
		Size: 5.5 MB (5544906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ceab62b056e368760dc0a031792b7745ae4966225a33ddc1cb15cb47550ad`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9000337c3a99f635eafb642bd725f4542ee547c959d7e0021b352c6d716fad8`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c2f52ca3c7d3802e22e5a5983407c6e6b79cba6d7dd481854626f0d707286`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:5d1da82e27e5bee17e5b45f6eeb635392ac9a080e0ffb88051891a507614ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9558020a63545edf61ceb921d1a712558df7bda3b970526191a367331eb66921
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97568213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdb45ee65acf6c0bce72f059897f9b17f7f7e4a4574ffe26994ba5e7c054c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
# Mon, 23 Mar 2020 21:37:23 GMT
RUN apk add --no-cache iproute2
# Mon, 23 Mar 2020 21:37:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 23 Mar 2020 21:37:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 23 Mar 2020 21:37:27 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 23 Mar 2020 21:37:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 23 Mar 2020 21:37:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 23 Mar 2020 21:37:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Mar 2020 21:37:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a271affe02af7f7c17c21afea5a80c7a7beef90fd35d3d1b777a546efbc09`  
		Last Modified: Mon, 23 Mar 2020 21:38:30 GMT  
		Size: 737.8 KB (737788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e335660b237b8ba9e44067b870612e2d7bc537c0c44cb76817e3b1553ca143`  
		Last Modified: Mon, 23 Mar 2020 21:38:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bed69641936f2f620cfc29b51dbb90f205539edb8e12f7c764a9fcaa09025f`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993191c7a55ab3c67f49c847e77fc68b47ebd297d0df6cbe6a7cbcd9e1e290b7`  
		Last Modified: Mon, 23 Mar 2020 21:38:32 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e354682f72a669ca6ab57fdf4ebfbc2e813048e00372ae1cb173b996989e43`  
		Last Modified: Mon, 23 Mar 2020 21:38:31 GMT  
		Size: 13.2 MB (13154699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ff660f1e572dfe9c3db055dc0a27bd6976ebaa7bf27719af582483680ac309`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:c061e3894336ba0dbf26144b7d816f59cedb2d0304fb11cc8bab21f9fabcf4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:b13a275725f070a0bfcaf68ce6474ad47008ca29ff3d1de21836d342967e37bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86091642623aa4d51ccc77f196b7640513334cc07c79636d2c3648defb3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:47 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145837c41213d104c08dc578bbdcab4a9f23a403ff9bdd5285b54e339568287e`  
		Last Modified: Mon, 23 Mar 2020 21:38:40 GMT  
		Size: 8.2 MB (8158656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v6

```console
$ docker pull docker@sha256:7eb1117ebd89423822f0880254dbf87ee699d9a8efe0b07d82d95e3a372b99d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72258644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08be4718e8abfbb5d121202beb674a899eac334a25a973d73dbf3baf362513b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:06:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8d8b3216f7fcba0890fbe2e2c803188979a28a9cb7b8bc4550ff9bb1a9343`  
		Last Modified: Mon, 23 Mar 2020 22:07:17 GMT  
		Size: 7.8 MB (7782806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm variant v7

```console
$ docker pull docker@sha256:dbe9d61f34600e33e6bc49fad0c6ad63c770ea097b046378517faaf82d83cf85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754651b3b148fa5ef97050227c8ec8b6fa3f23f75fbe4467e0a0e06171f2c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:17:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6d158b95a40b14d93047b67c03bee7d0d66d9dff39b5016d34f3a9fa4c01`  
		Last Modified: Mon, 23 Mar 2020 22:19:07 GMT  
		Size: 7.0 MB (7012560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c84b97ad756af72337727cb4e0b1269316b217dfeb27e5c6eeabaec4ad28a45a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70481944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7335b0dfaf0da2807689d7667205c01f848415edeb7fe5f8d793ba1fd04052e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:32 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd6cbbd7d27a1cb69e5062a96cd9f22877ad55d251d5ff5ce84a8480be0ea3`  
		Last Modified: Mon, 23 Mar 2020 22:03:34 GMT  
		Size: 8.4 MB (8354040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:afea2876df8334e5430d2427cfd37b39be2ee497db76d3651b2b14d97de4b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:aaead6545f3f63850ba8cbd1cf9cbe85e0cc9a512ec4d23060b0b69c5d72680e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2e482e9de9ca3939dce4c90810c89fa7e7450f774590967c2908cba857ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:f5e47dbe2b0e0c18a594b8f963bee76a360d900cc8ba83a6e00afecb2e4d4c02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679551e5cdc51461a4b78e1f8ce583384562f2acbbfd7655012853993740f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:9578d4c298343d2083bf58baafac2923eb9ceb109ab0b879ee502b380cb48384
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26135427427a7f96bf806d0b05d2c5d8145d2ee1fa8a74cf95f520b72060624a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8050f22a8d227118300d650bde0c3a1d418b98ac72962d933419f878384bc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e59ae775d55303c7e29acd62f3a1764673c91d4436b4232d427a38d5cf6277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable`

```console
$ docker pull docker@sha256:afea2876df8334e5430d2427cfd37b39be2ee497db76d3651b2b14d97de4b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable` - linux; amd64

```console
$ docker pull docker@sha256:aaead6545f3f63850ba8cbd1cf9cbe85e0cc9a512ec4d23060b0b69c5d72680e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2e482e9de9ca3939dce4c90810c89fa7e7450f774590967c2908cba857ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v6

```console
$ docker pull docker@sha256:f5e47dbe2b0e0c18a594b8f963bee76a360d900cc8ba83a6e00afecb2e4d4c02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679551e5cdc51461a4b78e1f8ce583384562f2acbbfd7655012853993740f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm variant v7

```console
$ docker pull docker@sha256:9578d4c298343d2083bf58baafac2923eb9ceb109ab0b879ee502b380cb48384
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26135427427a7f96bf806d0b05d2c5d8145d2ee1fa8a74cf95f520b72060624a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8050f22a8d227118300d650bde0c3a1d418b98ac72962d933419f878384bc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e59ae775d55303c7e29acd62f3a1764673c91d4436b4232d427a38d5cf6277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-dind`

```console
$ docker pull docker@sha256:ba51388db2907f0f0d33b365f039f89b48bfe9e3a408c2211addd5357268f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-dind` - linux; amd64

```console
$ docker pull docker@sha256:ad5b5195369a35265a33701ebea33065fa4c444de99bddece07637cff061afd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74564667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e51fd179fb849f4ec6faee318101d32830103f5615215716bd686c56afaea1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c9557e5f2b9b8fa553aa6f907a6d12f2217591cef74462b52e2e9d6bbb23ace3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a39444acd2e083ced4230738bb4707c7c3b7f7d6726e313d160b6f6543283d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:05:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:05:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:05:55 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:05:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:05:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:58 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:05:59 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:06:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:06:00 GMT
CMD []
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7ba7497a4c01d268a06a05014b168ac1cb74413c6e0ae710ad3469530c89c`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 3.2 MB (3160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5904ee04ec79e4943102f425fc2f4d79499f8ec03fdb360017c7cfdba8d05be`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe794901e085309747f4f7be9ecbc65c7c1b6f9e8ea863309588d3593115139`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c876279fc6bc524f2a67d73903959bf8d6b566159fbc4375d46de90534bf892`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29d8e06c8142bacc57bcf2bc3a1699f714e8896eab373c818af9ed53c2f65377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67002022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fc21e7e3d4d6ca3ac07203e6db78cdec4c686619b7f96ace77896164ea007`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:16:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:16:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:16:48 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:16:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:16:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:17:03 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:17:07 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:17:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:17:20 GMT
CMD []
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe56a4b6c1f198928eca7534f4247591aa211cd3d569187330b5c19783d171`  
		Last Modified: Mon, 23 Mar 2020 22:18:49 GMT  
		Size: 2.8 MB (2824370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932c1314c55e1e27c3d804ffffcce7b03a320adeebf297080709ea75795aa70`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62999c7314ddbf68e6aab71c9d95eb4ad7656b186eb79e2b5c966781e9521b3e`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 751.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52386e4e869ce89244a2e79701b0d07d531edc12fead5e7659c2ec2c9d63dc`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79b64df37e8a4dd5caa6f4425e92968af863d8aed47cf92045a660926ae4530c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01edd0e422bca03945f4e087ab929db62bc948338682b5a4d8f85d214c301b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:02:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:02:20 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:02:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:02:22 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:22 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:02:23 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:02:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:24 GMT
CMD []
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efd0796f1d1e7e4bce8afa5e864062d575e574570cbdb39b5deab65202fb353`  
		Last Modified: Mon, 23 Mar 2020 22:03:21 GMT  
		Size: 5.5 MB (5544906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ceab62b056e368760dc0a031792b7745ae4966225a33ddc1cb15cb47550ad`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9000337c3a99f635eafb642bd725f4542ee547c959d7e0021b352c6d716fad8`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c2f52ca3c7d3802e22e5a5983407c6e6b79cba6d7dd481854626f0d707286`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-dind-rootless`

```console
$ docker pull docker@sha256:5d1da82e27e5bee17e5b45f6eeb635392ac9a080e0ffb88051891a507614ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:stable-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9558020a63545edf61ceb921d1a712558df7bda3b970526191a367331eb66921
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97568213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdb45ee65acf6c0bce72f059897f9b17f7f7e4a4574ffe26994ba5e7c054c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
# Mon, 23 Mar 2020 21:37:23 GMT
RUN apk add --no-cache iproute2
# Mon, 23 Mar 2020 21:37:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 23 Mar 2020 21:37:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 23 Mar 2020 21:37:27 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 23 Mar 2020 21:37:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 23 Mar 2020 21:37:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 23 Mar 2020 21:37:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Mar 2020 21:37:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a271affe02af7f7c17c21afea5a80c7a7beef90fd35d3d1b777a546efbc09`  
		Last Modified: Mon, 23 Mar 2020 21:38:30 GMT  
		Size: 737.8 KB (737788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e335660b237b8ba9e44067b870612e2d7bc537c0c44cb76817e3b1553ca143`  
		Last Modified: Mon, 23 Mar 2020 21:38:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bed69641936f2f620cfc29b51dbb90f205539edb8e12f7c764a9fcaa09025f`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993191c7a55ab3c67f49c847e77fc68b47ebd297d0df6cbe6a7cbcd9e1e290b7`  
		Last Modified: Mon, 23 Mar 2020 21:38:32 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e354682f72a669ca6ab57fdf4ebfbc2e813048e00372ae1cb173b996989e43`  
		Last Modified: Mon, 23 Mar 2020 21:38:31 GMT  
		Size: 13.2 MB (13154699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ff660f1e572dfe9c3db055dc0a27bd6976ebaa7bf27719af582483680ac309`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:stable-git`

```console
$ docker pull docker@sha256:c061e3894336ba0dbf26144b7d816f59cedb2d0304fb11cc8bab21f9fabcf4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:stable-git` - linux; amd64

```console
$ docker pull docker@sha256:b13a275725f070a0bfcaf68ce6474ad47008ca29ff3d1de21836d342967e37bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86091642623aa4d51ccc77f196b7640513334cc07c79636d2c3648defb3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:47 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145837c41213d104c08dc578bbdcab4a9f23a403ff9bdd5285b54e339568287e`  
		Last Modified: Mon, 23 Mar 2020 21:38:40 GMT  
		Size: 8.2 MB (8158656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:7eb1117ebd89423822f0880254dbf87ee699d9a8efe0b07d82d95e3a372b99d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72258644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08be4718e8abfbb5d121202beb674a899eac334a25a973d73dbf3baf362513b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:06:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8d8b3216f7fcba0890fbe2e2c803188979a28a9cb7b8bc4550ff9bb1a9343`  
		Last Modified: Mon, 23 Mar 2020 22:07:17 GMT  
		Size: 7.8 MB (7782806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:dbe9d61f34600e33e6bc49fad0c6ad63c770ea097b046378517faaf82d83cf85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754651b3b148fa5ef97050227c8ec8b6fa3f23f75fbe4467e0a0e06171f2c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:17:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6d158b95a40b14d93047b67c03bee7d0d66d9dff39b5016d34f3a9fa4c01`  
		Last Modified: Mon, 23 Mar 2020 22:19:07 GMT  
		Size: 7.0 MB (7012560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:stable-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c84b97ad756af72337727cb4e0b1269316b217dfeb27e5c6eeabaec4ad28a45a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70481944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7335b0dfaf0da2807689d7667205c01f848415edeb7fe5f8d793ba1fd04052e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:32 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd6cbbd7d27a1cb69e5062a96cd9f22877ad55d251d5ff5ce84a8480be0ea3`  
		Last Modified: Mon, 23 Mar 2020 22:03:34 GMT  
		Size: 8.4 MB (8354040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test`

```console
$ docker pull docker@sha256:afea2876df8334e5430d2427cfd37b39be2ee497db76d3651b2b14d97de4b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test` - linux; amd64

```console
$ docker pull docker@sha256:aaead6545f3f63850ba8cbd1cf9cbe85e0cc9a512ec4d23060b0b69c5d72680e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69015945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2e482e9de9ca3939dce4c90810c89fa7e7450f774590967c2908cba857ddd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm variant v6

```console
$ docker pull docker@sha256:f5e47dbe2b0e0c18a594b8f963bee76a360d900cc8ba83a6e00afecb2e4d4c02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64475838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d679551e5cdc51461a4b78e1f8ce583384562f2acbbfd7655012853993740f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm variant v7

```console
$ docker pull docker@sha256:9578d4c298343d2083bf58baafac2923eb9ceb109ab0b879ee502b380cb48384
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64173058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26135427427a7f96bf806d0b05d2c5d8145d2ee1fa8a74cf95f520b72060624a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8050f22a8d227118300d650bde0c3a1d418b98ac72962d933419f878384bc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e59ae775d55303c7e29acd62f3a1764673c91d4436b4232d427a38d5cf6277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-dind`

```console
$ docker pull docker@sha256:ba51388db2907f0f0d33b365f039f89b48bfe9e3a408c2211addd5357268f33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-dind` - linux; amd64

```console
$ docker pull docker@sha256:ad5b5195369a35265a33701ebea33065fa4c444de99bddece07637cff061afd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74564667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e51fd179fb849f4ec6faee318101d32830103f5615215716bd686c56afaea1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c9557e5f2b9b8fa553aa6f907a6d12f2217591cef74462b52e2e9d6bbb23ace3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67641158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a39444acd2e083ced4230738bb4707c7c3b7f7d6726e313d160b6f6543283d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:05:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:05:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:05:55 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:05:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:05:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:58 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:05:59 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:06:00 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:06:00 GMT
CMD []
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7ba7497a4c01d268a06a05014b168ac1cb74413c6e0ae710ad3469530c89c`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 3.2 MB (3160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5904ee04ec79e4943102f425fc2f4d79499f8ec03fdb360017c7cfdba8d05be`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe794901e085309747f4f7be9ecbc65c7c1b6f9e8ea863309588d3593115139`  
		Last Modified: Mon, 23 Mar 2020 22:07:02 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c876279fc6bc524f2a67d73903959bf8d6b566159fbc4375d46de90534bf892`  
		Last Modified: Mon, 23 Mar 2020 22:07:01 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29d8e06c8142bacc57bcf2bc3a1699f714e8896eab373c818af9ed53c2f65377
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67002022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fc21e7e3d4d6ca3ac07203e6db78cdec4c686619b7f96ace77896164ea007`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:16:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:16:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:16:48 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:16:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:16:57 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:17:03 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:17:07 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:17:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:17:20 GMT
CMD []
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe56a4b6c1f198928eca7534f4247591aa211cd3d569187330b5c19783d171`  
		Last Modified: Mon, 23 Mar 2020 22:18:49 GMT  
		Size: 2.8 MB (2824370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932c1314c55e1e27c3d804ffffcce7b03a320adeebf297080709ea75795aa70`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62999c7314ddbf68e6aab71c9d95eb4ad7656b186eb79e2b5c966781e9521b3e`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 751.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b52386e4e869ce89244a2e79701b0d07d531edc12fead5e7659c2ec2c9d63dc`  
		Last Modified: Mon, 23 Mar 2020 22:18:48 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79b64df37e8a4dd5caa6f4425e92968af863d8aed47cf92045a660926ae4530c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01edd0e422bca03945f4e087ab929db62bc948338682b5a4d8f85d214c301b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 22:02:19 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 22:02:20 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 22:02:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 22:02:22 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:22 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 22:02:23 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 22:02:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:24 GMT
CMD []
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efd0796f1d1e7e4bce8afa5e864062d575e574570cbdb39b5deab65202fb353`  
		Last Modified: Mon, 23 Mar 2020 22:03:21 GMT  
		Size: 5.5 MB (5544906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ceab62b056e368760dc0a031792b7745ae4966225a33ddc1cb15cb47550ad`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9000337c3a99f635eafb642bd725f4542ee547c959d7e0021b352c6d716fad8`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85c2f52ca3c7d3802e22e5a5983407c6e6b79cba6d7dd481854626f0d707286`  
		Last Modified: Mon, 23 Mar 2020 22:03:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-dind-rootless`

```console
$ docker pull docker@sha256:5d1da82e27e5bee17e5b45f6eeb635392ac9a080e0ffb88051891a507614ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:test-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9558020a63545edf61ceb921d1a712558df7bda3b970526191a367331eb66921
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97568213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdb45ee65acf6c0bce72f059897f9b17f7f7e4a4574ffe26994ba5e7c054c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 23 Mar 2020 21:37:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:16 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 23 Mar 2020 21:37:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 23 Mar 2020 21:37:17 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:17 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Mar 2020 21:37:18 GMT
EXPOSE 2375 2376
# Mon, 23 Mar 2020 21:37:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:18 GMT
CMD []
# Mon, 23 Mar 2020 21:37:23 GMT
RUN apk add --no-cache iproute2
# Mon, 23 Mar 2020 21:37:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 23 Mar 2020 21:37:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 23 Mar 2020 21:37:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 23 Mar 2020 21:37:27 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 23 Mar 2020 21:37:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 23 Mar 2020 21:37:40 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 23 Mar 2020 21:37:40 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Mar 2020 21:37:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700258d9d0b34a9ffb647568e2f5cb20e68b4aa417550fea1a2e05f7a60593`  
		Last Modified: Mon, 23 Mar 2020 21:38:21 GMT  
		Size: 5.5 MB (5544154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a414fd7e40782db3c565da8385738c04271b9f80041f98ebaf9e11863a94542c`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffe6ac9a7ca617e0668cb7c0b3138e282168a1820661ff1d50982882ca72255`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d9a51a3887e53b6b428247af6d606d78d3ceb81ffa04fde41152097d02366`  
		Last Modified: Mon, 23 Mar 2020 21:38:20 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a271affe02af7f7c17c21afea5a80c7a7beef90fd35d3d1b777a546efbc09`  
		Last Modified: Mon, 23 Mar 2020 21:38:30 GMT  
		Size: 737.8 KB (737788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e335660b237b8ba9e44067b870612e2d7bc537c0c44cb76817e3b1553ca143`  
		Last Modified: Mon, 23 Mar 2020 21:38:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bed69641936f2f620cfc29b51dbb90f205539edb8e12f7c764a9fcaa09025f`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993191c7a55ab3c67f49c847e77fc68b47ebd297d0df6cbe6a7cbcd9e1e290b7`  
		Last Modified: Mon, 23 Mar 2020 21:38:32 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e354682f72a669ca6ab57fdf4ebfbc2e813048e00372ae1cb173b996989e43`  
		Last Modified: Mon, 23 Mar 2020 21:38:31 GMT  
		Size: 13.2 MB (13154699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ff660f1e572dfe9c3db055dc0a27bd6976ebaa7bf27719af582483680ac309`  
		Last Modified: Mon, 23 Mar 2020 21:38:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:test-git`

```console
$ docker pull docker@sha256:c061e3894336ba0dbf26144b7d816f59cedb2d0304fb11cc8bab21f9fabcf4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-git` - linux; amd64

```console
$ docker pull docker@sha256:b13a275725f070a0bfcaf68ce6474ad47008ca29ff3d1de21836d342967e37bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77174601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86091642623aa4d51ccc77f196b7640513334cc07c79636d2c3648defb3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:37:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 21:37:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 21:37:02 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 21:37:03 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 21:37:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 21:37:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 21:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 21:37:09 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 21:37:47 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69846a6807b33aed762f50d8ece72eebe0c64fe01a1faafaca5a2c415adc528a`  
		Last Modified: Mon, 23 Mar 2020 21:38:00 GMT  
		Size: 2.0 MB (1992001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517540127c623a2120eda3cab34123c21b433433be5ff4bda9e706bd9a802ac`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4bc653673c773e6afddafeeed0a06b909c8e894097a027c6df76055e18af9f`  
		Last Modified: Mon, 23 Mar 2020 21:38:13 GMT  
		Size: 64.2 MB (64218860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a82484b25481939587675e823ada105e54b607c43b43fa2c21baf5e4d7db7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7178a08bc331c10bd69447bae5c060dc7ff12993482c12646cf611fb1cbb7`  
		Last Modified: Mon, 23 Mar 2020 21:37:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fedb666dd1a7aaf5de730dbc25e0125fc5bd59e31341d7baa65acc0f9780b3`  
		Last Modified: Mon, 23 Mar 2020 21:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145837c41213d104c08dc578bbdcab4a9f23a403ff9bdd5285b54e339568287e`  
		Last Modified: Mon, 23 Mar 2020 21:38:40 GMT  
		Size: 8.2 MB (8158656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:7eb1117ebd89423822f0880254dbf87ee699d9a8efe0b07d82d95e3a372b99d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72258644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08be4718e8abfbb5d121202beb674a899eac334a25a973d73dbf3baf362513b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:05:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:05:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:05:27 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:05:28 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:05:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:05:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:05:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:05:43 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:06:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf8642eff4a9495d4e849e9cb15569c460dd7787b1105c0caf2ad25bedf5a2`  
		Last Modified: Mon, 23 Mar 2020 22:06:30 GMT  
		Size: 1.9 MB (1928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436d18c19aafe5702fad8c07b8e6da26b989af76e6c6aa89393641b37faa88d3`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c1347b48590f1bdc5f30aa8fe6091fa7349d12ed6403da81d92de04c98a248`  
		Last Modified: Mon, 23 Mar 2020 22:06:49 GMT  
		Size: 59.9 MB (59927155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53f975b9371cd55ed32a931972fecd6475836b36a53a8c8ab39ae41100eb7e`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2835f61d34c961e3625772ed6033c8dd06fe71ce78f3a7f9f4b042f7810b072f`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ebd8c45258b2482114fcb232fb082845f859f0ad1a2bd15dd08cd4ed0859d`  
		Last Modified: Mon, 23 Mar 2020 22:06:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8d8b3216f7fcba0890fbe2e2c803188979a28a9cb7b8bc4550ff9bb1a9343`  
		Last Modified: Mon, 23 Mar 2020 22:07:17 GMT  
		Size: 7.8 MB (7782806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:dbe9d61f34600e33e6bc49fad0c6ad63c770ea097b046378517faaf82d83cf85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71185618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6754651b3b148fa5ef97050227c8ec8b6fa3f23f75fbe4467e0a0e06171f2c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:14:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:14:47 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:14:49 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:15:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:15:15 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:15:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:15:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:15:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:16:10 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:17:51 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59e9eda66a43331e382fb0e3a3ec1ba9a3d1a2f115674b69dcafbbd3a3e8cf`  
		Last Modified: Mon, 23 Mar 2020 22:18:15 GMT  
		Size: 1.8 MB (1823645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b4da60b25e540f5d2e185d1334bf6b1e81a48441ef8068676800e9126046a`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328724de9c7193870415fc23e2eee3c4b4a52c8f5b79c13ee5282fb78e5c65eb`  
		Last Modified: Mon, 23 Mar 2020 22:18:34 GMT  
		Size: 59.9 MB (59927055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cae79a5b485887bbb85a65516c9233358f4663c39b8132f79ce83f2e6409bab`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bce3e91750bc0645060a96fae72300a343183da706325b2ed95a8f36202987`  
		Last Modified: Mon, 23 Mar 2020 22:18:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a640ceff2b20a6699b28424a948ff63c466d4ad53b726237dde25825ad77a9`  
		Last Modified: Mon, 23 Mar 2020 22:18:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6d158b95a40b14d93047b67c03bee7d0d66d9dff39b5016d34f3a9fa4c01`  
		Last Modified: Mon, 23 Mar 2020 22:19:07 GMT  
		Size: 7.0 MB (7012560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c84b97ad756af72337727cb4e0b1269316b217dfeb27e5c6eeabaec4ad28a45a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70481944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7335b0dfaf0da2807689d7667205c01f848415edeb7fe5f8d793ba1fd04052e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:01:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Mon, 23 Mar 2020 22:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 23 Mar 2020 22:01:51 GMT
ENV DOCKER_VERSION=19.03.8
# Mon, 23 Mar 2020 22:02:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 23 Mar 2020 22:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 23 Mar 2020 22:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 23 Mar 2020 22:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Mar 2020 22:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 23 Mar 2020 22:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2020 22:02:08 GMT
CMD ["sh"]
# Mon, 23 Mar 2020 22:02:32 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726da4a27347ff9ea9a752daf57239f4f8cda9976154e9927eb933946ceccae`  
		Last Modified: Mon, 23 Mar 2020 22:02:50 GMT  
		Size: 2.0 MB (2015646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3cb2b3a465287d7eed506f20be410e5a61bd9cc51fdb381fef41e550b8921`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8135161ac30008d4d71aaf0fe17b3dac875143e0dc4595a731d1948a9d85b4`  
		Last Modified: Mon, 23 Mar 2020 22:03:08 GMT  
		Size: 57.4 MB (57387259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938096eeda7197d9b062acf9b2aa9aef5771fe461dc3219be99fb897254936b`  
		Last Modified: Mon, 23 Mar 2020 22:02:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648c0e7fc3a89a9b0d1ec0d29bde2331c9ed615d6076ea4d200b7a325187559c`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85cdb0d7dce4d85ef9fb121c8a7d715615da6339688638f183dc7d2302f3df`  
		Last Modified: Mon, 23 Mar 2020 22:02:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd6cbbd7d27a1cb69e5062a96cd9f22877ad55d251d5ff5ce84a8480be0ea3`  
		Last Modified: Mon, 23 Mar 2020 22:03:34 GMT  
		Size: 8.4 MB (8354040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

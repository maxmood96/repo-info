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

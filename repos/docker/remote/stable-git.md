## `docker:stable-git`

```console
$ docker pull docker@sha256:e888a35bbc13b15805d2c037f49a3491828a840fe642c80b65ac13ef71eab723
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
$ docker pull docker@sha256:bc0b0d405c1e2c6b365d09246756d2d4df5863ead71ff37cde0395e18832b525
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72273342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c69c34b8489345075587336e4f61de4c56072dd09e3f5d4a9ba6d2f9f4f5f`
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
# Thu, 23 Apr 2020 17:13:45 GMT
RUN apk add --no-cache git
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
	-	`sha256:59b7cb0ba4509eedc92c81006ddcf0e45d6676a0750dc0867dec331c7d6feb44`  
		Last Modified: Thu, 23 Apr 2020 17:14:54 GMT  
		Size: 7.8 MB (7797688 bytes)  
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

## `docker:23-dind-rootless`

```console
$ docker pull docker@sha256:0efb72251205581d4b207036415a510c3bc08526b8ab313426901b87a4ce60b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:23-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5685cdce034a91d3d13846ab049e7e8e7758f8ebb24d6d697733f1944d3e819a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137408056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7444e9281f477cb0c5803a6f598d3cb71d82be8d05563f3cb228c148d77044`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.21.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-x86_64'; 			sha256='08e549924823e97a3ea303c2309b812dfd5223b8be5ff96fe41bf75181ce0977'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv6'; 			sha256='058ec96bc81ddeb317d160a6dea5bd8ac65dc2e90afff86bcc31f3f818f3fc5a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv7'; 			sha256='d46dbbbf5723c45125277c7c75b757b22679962707b2276a6d52f35964583c42'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-aarch64'; 			sha256='5daf8d1a04cd649ad4a64221d0ca0cffcce33c740e60d5b15698545ce6d0436b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-ppc64le'; 			sha256='fadbb72890d72f1246b213c453ec90cf494f4f8ea3dda2f63678de53a7e97c15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-riscv64'; 			sha256='cd01536476864bd97c6ce3dfd317730535e51b2e252e9468de0379cc84298187'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-s390x'; 			sha256='dfa8ab3ccc83311a2a4fddc43654de06c13cadc7caf629a0ddeceabd24bb6308'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc637b43d9a1be530bbb0bf04f5aa2df0db03a9d8a859d2d73978ba76458922`  
		Last Modified: Fri, 01 Sep 2023 00:51:11 GMT  
		Size: 2.0 MB (2014300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da631a25380a3953c3ec26b068605c249a9c215185b8eba2ff2d46d41b10dda0`  
		Last Modified: Fri, 01 Sep 2023 00:51:12 GMT  
		Size: 16.3 MB (16250855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b80e8b6f4e1be7904b02b165da4cecbb88d3c348f6b21b7e7cd1a53592b63`  
		Last Modified: Fri, 01 Sep 2023 00:51:12 GMT  
		Size: 17.5 MB (17459266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc33a04a2972155da94cd07359a286009e0b946df933f8b8c65b130791a5ab8`  
		Last Modified: Fri, 01 Sep 2023 00:51:12 GMT  
		Size: 17.8 MB (17826592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36dd47a681e936eca6a43360cbe56501d3f438562a064ecb699803375b7d6e9`  
		Last Modified: Fri, 01 Sep 2023 00:51:12 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4761ac4fc32b8d5624cca364ae27bce2efb1df033cdd391b36eaab03aae82cd0`  
		Last Modified: Fri, 01 Sep 2023 00:51:13 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2469fd65498eb05d0318616cdadda08526c43e2e39f71c75a30c1e7218e378cf`  
		Last Modified: Fri, 01 Sep 2023 00:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad99793fbd9b04163cad774b87c413299117aec041e69c945a5fc40b5ce254ad`  
		Last Modified: Fri, 01 Sep 2023 01:50:55 GMT  
		Size: 7.1 MB (7080264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad957e8578f59bfee255ac5f5fda8c22bf42d33f13986b884ccbe9021b3a6ba`  
		Last Modified: Fri, 01 Sep 2023 01:50:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023311cdc3039f563a8bd5c76da58faef61e97a33601a5454d12076ea57506f2`  
		Last Modified: Fri, 01 Sep 2023 01:50:57 GMT  
		Size: 51.7 MB (51657451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26212cc9ab730f476b8497344849ecc2f7d9d8f65c1a4ffbb455fbf9ad92cc11`  
		Last Modified: Fri, 01 Sep 2023 01:50:55 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1e8099f0170ae6d195eaccdbb7041e138fa32b195d7d76f769490774556e5a`  
		Last Modified: Fri, 01 Sep 2023 01:50:56 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afedb221fdf37ae0f1e9c505511ef57e6c5e0d47fdd221870dd730e2e109aa0`  
		Last Modified: Fri, 01 Sep 2023 02:51:23 GMT  
		Size: 1.4 MB (1362170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18089b3504d00bb82232946c72809e37a7ffd275ccdbb782ff01cfff2b726b2c`  
		Last Modified: Fri, 01 Sep 2023 02:51:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b511fcf6d96c10e4425b245b9f675077e1cc852af71bf9a2193a86adacb32281`  
		Last Modified: Fri, 01 Sep 2023 02:51:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e53cfd232b06ea5e2d6b9985459f0232248392f329800cf0709cb7daec3228e`  
		Last Modified: Fri, 01 Sep 2023 02:51:24 GMT  
		Size: 20.3 MB (20347085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a17494bfe75af1afdda085b158cabc695256f95e1e1f72140ec0b62c3d136`  
		Last Modified: Fri, 01 Sep 2023 02:51:24 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:23-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1845e393b72e87398df05762530a78bfab55609a641f3d1c4b7c818ac0fe4c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.0 KB (861953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af612d3539418ab94d1d9bd702f1518af14b50731fd782d912bfd642bc8f549f`

```dockerfile
```

-	Layers:
	-	`sha256:a641bf550c419e106c9e59888b84016322fd59b3f3bcfd2698d11faa89cb3d02`  
		Last Modified: Fri, 01 Sep 2023 02:51:22 GMT  
		Size: 831.2 KB (831171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1178b9b6750fe46ad33765db0a23a8cd503f821825fcb33a2c4928eab4a323c2`  
		Last Modified: Fri, 01 Sep 2023 02:51:22 GMT  
		Size: 30.8 KB (30782 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:23-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4a9320d6595a3a08eb0f4fd5b76df08deb7a926bc292585da944319b055de843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130739347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4226b7ecd248fcaaec7d3da2d950134dd61168f9b86e81ace89077dbcd4d8d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.21.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-x86_64'; 			sha256='08e549924823e97a3ea303c2309b812dfd5223b8be5ff96fe41bf75181ce0977'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv6'; 			sha256='058ec96bc81ddeb317d160a6dea5bd8ac65dc2e90afff86bcc31f3f818f3fc5a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-armv7'; 			sha256='d46dbbbf5723c45125277c7c75b757b22679962707b2276a6d52f35964583c42'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-aarch64'; 			sha256='5daf8d1a04cd649ad4a64221d0ca0cffcce33c740e60d5b15698545ce6d0436b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-ppc64le'; 			sha256='fadbb72890d72f1246b213c453ec90cf494f4f8ea3dda2f63678de53a7e97c15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-riscv64'; 			sha256='cd01536476864bd97c6ce3dfd317730535e51b2e252e9468de0379cc84298187'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-linux-s390x'; 			sha256='dfa8ab3ccc83311a2a4fddc43654de06c13cadc7caf629a0ddeceabd24bb6308'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852f3ef0b5f9b77c7c21abf9035ed77c331514fd6aa1498370a5dbd3e2048b5`  
		Last Modified: Mon, 07 Aug 2023 22:18:57 GMT  
		Size: 2.0 MB (2024556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa0183f177eef4fbf1985af430c61c77b95421f027eea28f816b0cd1422c2a`  
		Last Modified: Mon, 07 Aug 2023 22:43:59 GMT  
		Size: 15.3 MB (15325086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee7e69ab8affe56e6a48d95a413242bda38be403d58d989c83afd66e5ecddeb`  
		Last Modified: Mon, 07 Aug 2023 22:43:59 GMT  
		Size: 15.8 MB (15768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98439dd41c1aa2b7fec01ebd8a6fe6f86d45d34d4b5b2ccc545e06906fba647`  
		Last Modified: Fri, 01 Sep 2023 01:26:14 GMT  
		Size: 16.3 MB (16283689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ea9f56271fd4efb66f5b4b2fcdbb6b1b8aa54e604a818c868c52839b263f26`  
		Last Modified: Fri, 01 Sep 2023 01:26:13 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b11eb1e2a4a15b54fb772482757aa25902417b1c7bb3a6d4cd2d448bed67fc`  
		Last Modified: Fri, 01 Sep 2023 01:26:13 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e04686a2b8186e69165cfba25ecf25de27cedf8b04aeb66d1c255a20b42fc1`  
		Last Modified: Fri, 01 Sep 2023 01:26:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9f8592f5afd6b0428ea754544c0f25dbbe002bdd4d3b3a561359c3243a10f3`  
		Last Modified: Fri, 01 Sep 2023 01:54:05 GMT  
		Size: 7.3 MB (7291227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64f6d12d924d63a583ef57b026e0f9787e44e11db209018fb9717130976318d`  
		Last Modified: Fri, 01 Sep 2023 01:54:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b442b3805385e684775ba79c8c2bd1d970dc27dfc91bb93fcb1682be82ebd71d`  
		Last Modified: Fri, 01 Sep 2023 01:54:07 GMT  
		Size: 47.1 MB (47053354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e809baabb04af80b58d47b7a5305af13149063e6f17ec1582240ad21e0b06e4`  
		Last Modified: Fri, 01 Sep 2023 01:54:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87225f99297ea1bba5f6b5f0690f23735b50437ab815abe02eb95619b385f18`  
		Last Modified: Fri, 01 Sep 2023 01:54:05 GMT  
		Size: 2.8 KB (2799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa08e1d66cf2432aa61153ab1551e2b7f406fd1d3c6c05d2709730afda00f66`  
		Last Modified: Fri, 01 Sep 2023 02:52:39 GMT  
		Size: 1.4 MB (1413171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabd9555022518db5cd6f9d6540f59399825142dddc3ea57fa3c3d9f060dfb98`  
		Last Modified: Fri, 01 Sep 2023 02:52:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e6681c4f34283f2117fca926ffb857a61052040f56edeaef4c5004ce8e65f4`  
		Last Modified: Fri, 01 Sep 2023 02:52:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9674110f5c8d3611567531a96e45c6886846e55968142de390f79c78ee3b5e3a`  
		Last Modified: Fri, 01 Sep 2023 02:52:41 GMT  
		Size: 22.2 MB (22240981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f87e3db6c8847ea6872129417eff4a723348a62e859eb403d7048a5a20cbb`  
		Last Modified: Fri, 01 Sep 2023 02:52:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:23-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:dadfcbcac2cfd433adc7b4142f881d8e12fef34e38715209087564bb244962d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.2 KB (862232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1b97e5b32958699e4888a985c6d305a5555fc451c26fe4212596b8441b64f5`

```dockerfile
```

-	Layers:
	-	`sha256:ffc1955cb4b44e1f9a25db9e7f684b5a6cb54c8d6e916ab85a68f3deb92acf53`  
		Last Modified: Fri, 01 Sep 2023 02:52:38 GMT  
		Size: 831.4 KB (831394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df79fc0ed374ce587fe85f134939287cfe4a3e0fe4b54f01a1b9dd3fd8f3ca2`  
		Last Modified: Fri, 01 Sep 2023 02:52:38 GMT  
		Size: 30.8 KB (30838 bytes)  
		MIME: application/vnd.in-toto+json

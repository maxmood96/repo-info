## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:6282e1467634e443fadc4b262e6461c2723b7b3899fa347513b26a6fccdfec8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d8415f6d0e6bc53835b31456312eccd8c2e76478c23bb8f05e96c2cb8f5ca979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163322168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7c92028c0f1b2aced49586905a6a2d5cfc1b9a34178edba5e1b456e33325be`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD ["sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD []
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4092129885943338580727bcccd98cd492638406030f5562691816f76c20c37`  
		Last Modified: Wed, 18 Jun 2025 16:36:43 GMT  
		Size: 8.2 MB (8207497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602d7f7e952f9ccbe9f6d196befea43db6b8d7ff8e8557cbccbd7840f45a71d`  
		Last Modified: Wed, 18 Jun 2025 16:36:50 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578f3cb1858df948d9c37bf6006f04a65f0bc4d80280fe72ef3ab096800e96a`  
		Last Modified: Wed, 18 Jun 2025 16:36:54 GMT  
		Size: 20.4 MB (20449419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef8d96d89c083f89c52d7e6ebc0610dca4ce7decf71890418df9083d57fb00c`  
		Last Modified: Wed, 18 Jun 2025 16:36:45 GMT  
		Size: 21.7 MB (21664160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de02c2615eca13dfb173c17a404bc7fcb67ce687e0077d0c6916803bf6e41d5e`  
		Last Modified: Wed, 18 Jun 2025 16:36:45 GMT  
		Size: 21.1 MB (21100669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7ee9775039a186b2a172600da19a3c6dd30ca74a1959006c2755a298a37e0`  
		Last Modified: Wed, 18 Jun 2025 16:36:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f311ecf237fd48956efddc27ccb6fb05249fdba9d29097fb2d80799717a3c`  
		Last Modified: Wed, 18 Jun 2025 16:36:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485bbe5c73a8ea0c0456e56110f896221c5c6cad95895af6a616938cc89538d6`  
		Last Modified: Wed, 18 Jun 2025 16:36:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650761810d4ad82252d64d2792369f6ed01dfb741bb9800dd984d0428841af24`  
		Last Modified: Wed, 18 Jun 2025 16:43:19 GMT  
		Size: 6.9 MB (6905595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634e091b336d84b21b4b0a72e3a736b22997ea391100f8301960606337248454`  
		Last Modified: Wed, 18 Jun 2025 16:43:19 GMT  
		Size: 90.5 KB (90488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1937081ea9585c616659cb2a5669c895c4641f2bd50f667387407aa50136111`  
		Last Modified: Wed, 18 Jun 2025 16:43:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689fa04031af2bae8493cd73db22078c137bee036f4842bc6df2e08bd5e73e5e`  
		Last Modified: Wed, 18 Jun 2025 16:43:26 GMT  
		Size: 62.5 MB (62518562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7043809f0211b11d4d6e10d9274a2408d18bf2e2b1cf5aa6e97e1aa966dfac`  
		Last Modified: Wed, 18 Jun 2025 16:43:17 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a531727811b6587c21eb203b1a8b39aba2d3f5c0d3efbbd39bf2057bfe6c8d02`  
		Last Modified: Wed, 18 Jun 2025 16:43:18 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d276406d238353deab5be882778aa9094c5873393f86db98a25a64bfef6f2d7`  
		Last Modified: Wed, 18 Jun 2025 17:08:30 GMT  
		Size: 993.3 KB (993279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8c36d2c1eda97a948d84404a633c38cb748cc806a50acfbf0e8b3ef5a0e34b`  
		Last Modified: Wed, 18 Jun 2025 17:08:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e39839d2ee94c67a1dc531d5ba85c92acaa1723b93d75b727816ae02cd5b1d2`  
		Last Modified: Wed, 18 Jun 2025 17:08:30 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cca1a310fa9489cf07c6b72ba178a5eb9ca7c1c85ccbcf5cb8815fbb87651c`  
		Last Modified: Wed, 18 Jun 2025 17:08:32 GMT  
		Size: 17.6 MB (17586161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbfcc6f581e724d5a7ea3877ac3a2c34199ee8c868b86dee238517567eda54d`  
		Last Modified: Wed, 18 Jun 2025 17:08:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c6eea7ed3ef9d2ec3ec62ab0014089b17fdad77a897807ce42b716025e296d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdf16e4d5eded54051399963d857fa36b05d1fa5a561e26809a063df9d25bc7`

```dockerfile
```

-	Layers:
	-	`sha256:3a7c2c843f30ed7a9d5ca84923f100af5b2ae05438212987e6bc1e5dd5c6b901`  
		Last Modified: Wed, 18 Jun 2025 20:08:18 GMT  
		Size: 30.2 KB (30203 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e09168c9be8a406583f8469ad7bdca609d02a212555b59330906271aeed13b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154535587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4217c60a2862c4d560fdf4c5be912e5c2809347a09c80ac27bbeb41c532eac`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD ["sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD []
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3a21ac25f0993b9b6eb1ef3b105bbde8cc74659df3ecf2b5ae668c764f2858`  
		Last Modified: Wed, 18 Jun 2025 17:36:59 GMT  
		Size: 8.2 MB (8228994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec2fdb47dda06fef4575abf618c8a4ec7c561844f4a01c468f799c1a613148`  
		Last Modified: Wed, 18 Jun 2025 17:36:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4999b9eb270672d92f3c5f0e936c6971599a605d8f810cabeac0e7ba68906e87`  
		Last Modified: Wed, 18 Jun 2025 17:36:59 GMT  
		Size: 19.3 MB (19258560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e22edd08d9492410c0f536b00a1b0ab0c1c4c7b03930e460630dc7c29745d9`  
		Last Modified: Wed, 18 Jun 2025 17:37:00 GMT  
		Size: 19.8 MB (19819421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af5115c33d80b8b10621d0a3fe76130411071e9f9a1958cdfd62b5b0a6c0e1b`  
		Last Modified: Wed, 18 Jun 2025 17:37:01 GMT  
		Size: 19.3 MB (19347263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc74dde736df28e52030cc833ae8ff26f4b02b35dcf953632535121a8de01794`  
		Last Modified: Wed, 18 Jun 2025 17:36:58 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a7fb9225c40a6d9ce22162179e7b412cb780a324bf9eed8706e056b0598073`  
		Last Modified: Wed, 18 Jun 2025 17:36:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a5c597bdd65b0794d7c47d3243f10286145971a28e2974cd4b4298745697a6`  
		Last Modified: Wed, 18 Jun 2025 17:37:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeb96a9595ca228163638605fe9eb01f0ce8bcf9ac1d717262abcf1eb39140d`  
		Last Modified: Wed, 18 Jun 2025 19:07:32 GMT  
		Size: 7.1 MB (7141538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64bd16d41283fcfc9f4e1632f44e885e11b294432e3762e9c5481d69ffb0471`  
		Last Modified: Wed, 18 Jun 2025 19:07:32 GMT  
		Size: 99.6 KB (99647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298b86a813959d07bac47a6ed87f5f4c9920d6a4a6039bf4927c5434a9dc85ce`  
		Last Modified: Wed, 18 Jun 2025 19:07:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72b4766e514b216cfd0bd3c3f0b408e013f828084bf77afa0c36878d3b77397`  
		Last Modified: Wed, 18 Jun 2025 19:07:34 GMT  
		Size: 57.5 MB (57454409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768c22970bb7cb16747bfbd1e24f3ed4d44e7b342e52d46a7ce0c75caa95278f`  
		Last Modified: Wed, 18 Jun 2025 19:07:31 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550f7974107a73e867dfe3d86779f3ec5d8a7e89f4e92f9af5ca8265be02ebc`  
		Last Modified: Wed, 18 Jun 2025 19:07:30 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ad1aa24422b3363afe35c406b3515a0a01aa34c9aab21e14648645223f3a66`  
		Last Modified: Wed, 18 Jun 2025 20:08:41 GMT  
		Size: 1.0 MB (1022998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a615ee21eb402c4fa9be98a5d9eef33a0d3cd2533d2df12d6f41e3c6ca660619`  
		Last Modified: Wed, 18 Jun 2025 20:08:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a5fa60cffc6ab7de5174dcd69a0bc1bf23426a9b16c664ba55ca4c2cc399a8`  
		Last Modified: Wed, 18 Jun 2025 20:08:41 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf26bba6d62363c1ac675d9bc0cbb22cb89e58b7f4cffdd2d022ce2b2467e1cf`  
		Last Modified: Wed, 18 Jun 2025 20:08:42 GMT  
		Size: 18.0 MB (18017323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba68b072be1eea0b36f9cf789a72a5a5e6ab4799fa8aae74be0f9a4e6a9b295`  
		Last Modified: Wed, 18 Jun 2025 20:08:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:41daa1d7deaac9d86bd3d9412b1b99f2a13e08d6a413ca11a26fc467d5142d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407998a9687c1240f7ec6d5b6494c76a0efa2172a5461583f69d2b2bb64e667a`

```dockerfile
```

-	Layers:
	-	`sha256:a2544a512e9ac3141e76dad385198280a66242f92bc8f0b7018ab7ae834ebb5e`  
		Last Modified: Wed, 18 Jun 2025 20:08:22 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:2c35052eae6465ab377e9cacc0d2e5f3f4fbcffa99ad8493950a5d262202b8fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ebbdc8d984e80889daa9c25123b38d121d3d52a5a15a6737911e9cfa9aa1b3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154639655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f9742fdb79bb8dff7b886b507d4f0e66808306db622c45e9210cd98d3e19a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ab03998fa774214de3f50fa9236afd6b9b3739a4ee8e0158c4c1026278e95b`  
		Last Modified: Fri, 12 Jul 2024 00:55:45 GMT  
		Size: 7.9 MB (7869226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cda72fc9fe4700ac51a2a3b29681d606831004c4d56659608babcea9970a5a`  
		Last Modified: Fri, 12 Jul 2024 00:55:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f593f88cfadf783109f399dd64af7127d03e10c33742111ad35fc1c9eb274918`  
		Last Modified: Fri, 12 Jul 2024 00:55:45 GMT  
		Size: 18.1 MB (18069833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073d51dd9347292f0acab4a98ed75f55a251a1b8999f97cf961d228ab4aa0491`  
		Last Modified: Fri, 12 Jul 2024 00:55:45 GMT  
		Size: 18.4 MB (18404634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11517b755f11c06c48e09774fd4c2c817a6facbf45cc63639ff3ce68bb54db6f`  
		Last Modified: Fri, 12 Jul 2024 00:55:46 GMT  
		Size: 18.8 MB (18792449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151556c344ac5334b5ea0036f375837c9e46b0423004bc0264c77dc8b00c97e6`  
		Last Modified: Fri, 12 Jul 2024 00:55:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391a99f1c3ad3907ead72862f269268e843eaad4629fe584d3a26fc82ac811a3`  
		Last Modified: Fri, 12 Jul 2024 00:55:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b60581dc63871471b3835702e3f19bbc11086791a3f805a45f4205b2a1ad2d`  
		Last Modified: Fri, 12 Jul 2024 00:55:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6fc8c94dc6549bb475ff2275e293919324e695cc4b468c7c304ecb7c61fc5e`  
		Last Modified: Fri, 12 Jul 2024 01:49:47 GMT  
		Size: 9.1 MB (9061195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e2f9d4c4dae6fbbfbd8618148c394f2d4c208bd8ce6aaf73ac0b5aebceebc9`  
		Last Modified: Fri, 12 Jul 2024 01:49:47 GMT  
		Size: 89.3 KB (89264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0187015e66d8c8c149b6f36602b9a91ae1169e3fd772f586ee7ff16b7b7eb084`  
		Last Modified: Fri, 12 Jul 2024 01:49:47 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114e58d33eff2101f72b08080f3eb3cca917a0f675b07f6de7fe8821404209d9`  
		Last Modified: Fri, 12 Jul 2024 01:49:48 GMT  
		Size: 56.8 MB (56756508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928e873162845f30dfc858c253de3ce3f149b17734e28b31d597c9317b95b72`  
		Last Modified: Fri, 12 Jul 2024 01:49:47 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bcb7950fd6f620bdd34be5ef94ce1fbe74fc82c5792db5a1f49707441d63bf`  
		Last Modified: Fri, 12 Jul 2024 01:49:47 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092dd4d32767d341f188ab253165302e021e6ae46db38e5d9dcb064f953fc86`  
		Last Modified: Fri, 12 Jul 2024 02:49:01 GMT  
		Size: 981.0 KB (981019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8ec0c11c99c73c967157142c8b076720f88a19399661225451e0deb6c388d2`  
		Last Modified: Fri, 12 Jul 2024 02:49:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8339ee74eff5b099521914fe39c410f5bfef4652c67d5c1f67e295221163b53f`  
		Last Modified: Fri, 12 Jul 2024 02:49:01 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d7374b1d2b20da42f0fa25b60f77510ddc4f05a0ff98f23c7e56a5906036f`  
		Last Modified: Fri, 12 Jul 2024 02:49:02 GMT  
		Size: 21.0 MB (20982381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd51b0205b0e37a3cb6a36ed6dc3b870e86958a950bba1ba13e2578bb4f1ba9`  
		Last Modified: Fri, 12 Jul 2024 02:49:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:afa3083214eb9e6aa65c75d334463c95e7d6748e052066ea52a8b38eef2117ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377121173b54d9acc737e66f45107e6393510a6db37092f2c1829ec9bd2aa57`

```dockerfile
```

-	Layers:
	-	`sha256:5eb18abc3c8b3216d73d141747ffd5a8f4f75e946c9dd01109ac9367caec832c`  
		Last Modified: Fri, 12 Jul 2024 02:49:01 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:061604a48ddbf8dfd1a2e5c44a37a221011caacdb06b64a860aabb15dcd29dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149238103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc3130b971d6090505fb50071b7db41699fe1a9b3fcc4fe1622121359a9336f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2649985fe95ea7b64683a03a22cda12e6203403323506a2605bda4c9ad56ec1f`  
		Last Modified: Thu, 18 Jul 2024 18:57:02 GMT  
		Size: 8.0 MB (7974739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69fb4b09a403c091ca2d24994a101bc49383215888dcbd2752c99875fc041f5`  
		Last Modified: Thu, 18 Jul 2024 18:57:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c88eb84e2d7256c8b8e1d0553776d90243a05c06711507817c708f13f96738d`  
		Last Modified: Thu, 18 Jul 2024 18:57:02 GMT  
		Size: 17.0 MB (17028616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2fc95335a70f70bf04530ed6321de63f5c56e99937306967a67a8e7571d99e`  
		Last Modified: Thu, 18 Jul 2024 18:57:02 GMT  
		Size: 16.8 MB (16772841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e842971f67e2362316c68cd0bb2da89ba994a63d2068555c01d88753d3d5c8`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 17.2 MB (17176039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358f5d7c7199465ed20bb662ed738ef00e789061fced25842ac2af29116a9847`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19a53c6e2a7a1c4194974b68c31a3e65fab364065d5d956093f7c39727c13ab`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa34ff7d1ccb40b1cae26b9b4511586c675a36c34ff61b9d9c4eb7125bfdbb0`  
		Last Modified: Thu, 18 Jul 2024 18:57:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ba16056c3d6384550238b7f1f5e518f4280c1c7db0b91740a802fb39f8f841`  
		Last Modified: Thu, 18 Jul 2024 19:50:36 GMT  
		Size: 9.9 MB (9852931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa36c1802107d67d0056ff4ec219e8e50e99d3e6f43dd320612c7b8092f2d1a7`  
		Last Modified: Thu, 18 Jul 2024 19:50:36 GMT  
		Size: 98.7 KB (98690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd9a1ec338d665da183f0d9c775495dffab8d85d7fda4513d153223a6ba2c76`  
		Last Modified: Thu, 18 Jul 2024 19:50:35 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0179f9f1e378d129a2be40522ece8abfdb72b858cfe344f361840d67ff98446`  
		Last Modified: Thu, 18 Jul 2024 19:50:37 GMT  
		Size: 52.4 MB (52376009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e29ce00340ab663e0ac6c4ae5e3845f02f2d21919a3917ae2bd40043de692`  
		Last Modified: Thu, 18 Jul 2024 19:50:36 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1485648b620fe2590dc420fc493c98a8532d63005b3ee1facefa32dd5bb3b551`  
		Last Modified: Thu, 18 Jul 2024 19:50:37 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bea580436c0272436ba3fc4dfbcb3f7197e76d1d0e635b97ebf705c8c043a3d`  
		Last Modified: Thu, 18 Jul 2024 20:57:13 GMT  
		Size: 1.0 MB (1023189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40427297d755fe190c73c952c1352db7ccfb11def6b596dff348d323bfc526ed`  
		Last Modified: Thu, 18 Jul 2024 20:57:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edadb20049b956661bea1f3ff4cee5e3baabfe03c5bddf96d48eed15de53ed7f`  
		Last Modified: Thu, 18 Jul 2024 20:57:12 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab93dab133d1774c57502065c1675dd10c0cce04c8f1fe7707ead3a9267ddf1`  
		Last Modified: Thu, 18 Jul 2024 20:57:13 GMT  
		Size: 22.8 MB (22836955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d072e92946f3753562375e796e961edf8f14a8532714bad86eb093aeca89b02b`  
		Last Modified: Thu, 18 Jul 2024 20:57:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:919b83f120bdf9bb28a5fdfa1a113e4de09598f3bf30ee661b6d997e1f60d366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9642172186507d5497baf0a740be9a005e56b474270ac48734ca52b0b9beb08`

```dockerfile
```

-	Layers:
	-	`sha256:8d06ef25c07bc6d8002123a3f2d4f06e439f47616e63bafa5b81835b9af84fbf`  
		Last Modified: Thu, 18 Jul 2024 20:57:12 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

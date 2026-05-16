## `docker:dind-rootless`

```console
$ docker pull docker@sha256:2379588ca8e9ed0d452464f4aed5361da6361791ec1a2111d44515c3985b2659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:86dd1e4303fe60a2cd5f155db3c77e30011cfd8aaa9950188cece42d5e9f8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157179647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66937a706e25d69d45209cbd13b73c920e1d5ae4415214c93da738b95c779a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
# Sat, 16 May 2026 00:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3aecd32c9a7b429826161d546e29c1dff0ac6eea914337b0b9d0a168b785fe5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 3.4 MB (3420116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a1fd367a70907870ec61c5541633c1016315039aa85446173764ece77df84`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896453e7017b28888cd072db72945d8e744a934faf06c8d0afe071918a3ab492`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8de78d541dc09dba7c55cf30b416cc37bf4cadc540afd919f470b8c6ea68c5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 12.1 MB (12102497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ee9ce5b3abe899d1554ebbfe999955a855268f925239ee277ff0542c7424f`  
		Last Modified: Sat, 16 May 2026 00:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a928bb65ab1afe6b79776cfe5fec97b7de2ce78299935d0f2a6d93a022bbf33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10081df2ff0f054ec55a6ba8b0e73f3f8660a710ebcd84146466c7e415b001f2`

```dockerfile
```

-	Layers:
	-	`sha256:ef654a1e85deabbd5d572b1aa6d9feaba8a368d7af558b844574a48c0af89e2c`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:beddbc20555efb8bc7641a98e7a58a5104329118a81b075bd2373de0e1dca5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cb4b74b39f9eb3c077215fb0f4c6f7d8395bd86b29015b4743c1a5b13d2f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
# Sat, 16 May 2026 00:10:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7270b72b7f3e2799e7c141f64461907402307eab0e5a25271d1e2b47c44ee`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 3.4 MB (3394559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f6bb10aafb4e20e513a5cc5d9a7e3481a971f0433332b50708cd61bc4df70`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e8ff9e0e4eab7d4814e9d39e6a4c25f79d76d2979f00a78de155911ef2ddd`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91aab9887dd46e6f833ba3ffff294c32d59299ab8d4a3847194a60a227c55b0`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 11.2 MB (11236505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3459fdc6872a7acd1e3b7884a28a60561f9e3488cf19f8437a3b11c8e09a6d8`  
		Last Modified: Sat, 16 May 2026 00:10:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58ffdbbba10f97b2d1ef33dbfbdf016c2844506424a34f22333f5597310a7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a11fccc6bc4fd79d54dca7d1d3ed318788c65b63d3184fbb73c400cadceb60f`

```dockerfile
```

-	Layers:
	-	`sha256:fc110ccff973a2ba6b5d21f0f1f25d79b12b82a863abcabd81b546d627bb598c`  
		Last Modified: Sat, 16 May 2026 00:10:09 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

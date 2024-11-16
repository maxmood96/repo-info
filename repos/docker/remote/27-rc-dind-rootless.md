## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:2d376f28680cb87d6596087a308908773812742e029f401915c73643c982ea6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ee9cd00706edd28a2f96ef6ad24d04f4c20995eec0f7872adecbf8fb8ab4ed35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa5f37d41b157100212521762af1f3305baa4bcbb532e1874c537935e64c9a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD ["sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Sep 2024 16:05:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD []
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Sep 2024 16:05:47 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2bdf3e068f4036d4e620358993b9c593f8ff18d4cf94b49a476add064ba512`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 7.9 MB (7872607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d21d8593828d167c51c71bf0af81940e920a1e16c0998d7501a115a044bf9`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a56a2c1bc126e03aff15d92c21e6fbf4d72c087a0b342e3560796b818219a7e`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 18.6 MB (18563598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b768b567568f49cd31ed218304e59c4a8a5e490d5ba5977f5926ca7f2cb50b`  
		Last Modified: Wed, 18 Sep 2024 17:55:59 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3c0342b050b1723e6ff5c85ae2c709679e9fd4d1749f2a8547dac3384fbd09`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 19.0 MB (19035820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cb0511671bdcbd0a282c497fb55a7b5fbee3c6498d9ddc69488c9d0d2f590b`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d26317001f69b9168bfc04c3eaaad18b84ed642ca3a357a31cf5d82f9b79ba9`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6fa7486022ee24496533ed8f7f2472972769153f77d24ca0522e685407b3b`  
		Last Modified: Wed, 18 Sep 2024 17:56:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975b5daba5bd293c670c16319ff9387fd18a4eb23879a5f78af6da84b2ecc1d`  
		Last Modified: Wed, 18 Sep 2024 18:56:50 GMT  
		Size: 6.7 MB (6657937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a47492a2194494c4c0b5f7ac5fb325c503da90d4209a3b8cca3e4400f28939`  
		Last Modified: Wed, 18 Sep 2024 18:56:50 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19655f8d5d99eea638784a1122d6d405481c47437cbe294d9abaebc86689905`  
		Last Modified: Wed, 18 Sep 2024 18:56:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b436a4dfe40b37a080ef004cc5079cfb3c34dffa9296f9c70464c5e5bdf1ad`  
		Last Modified: Wed, 18 Sep 2024 18:56:50 GMT  
		Size: 57.8 MB (57798703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85730795b871ec1d3cefc23bf4bb0f0167efc669149368fe2aa4f9e47e8747d3`  
		Last Modified: Wed, 18 Sep 2024 18:56:50 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada2a0cae662c19937227037534e502f6996bdfe9848c802d4d5dfe8ea35ecfc`  
		Last Modified: Wed, 18 Sep 2024 18:56:50 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb2424892fbb1b662c7c66212478eb6c576c9a8e8f3be59ee286039c901405e`  
		Last Modified: Wed, 18 Sep 2024 20:58:41 GMT  
		Size: 981.0 KB (981009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2f582db1938d0d47bddf0d92d5a238ab219b7f26c969c4143b8ea6a9d2c2cf`  
		Last Modified: Wed, 18 Sep 2024 20:58:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a526405e34de2987ba77bd2b45f05a715e8007b1a23916db3531bdc0bd55a55a`  
		Last Modified: Wed, 18 Sep 2024 20:58:41 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4640f44f55eb6d94453e79f6e05bf6b245aa58ec372d57c3ed51165c58bb2f4`  
		Last Modified: Wed, 18 Sep 2024 20:58:42 GMT  
		Size: 21.3 MB (21303255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c3315cab08b94f715e239eac8750bc7e75cd996ec11488541aff999cc651b8`  
		Last Modified: Wed, 18 Sep 2024 20:58:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:cf08daf9635bff4ec5fc22724708dec0640f395a641ed0ccabe05a3c7b5f47ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da22d22a208a06f5daf5eff0027968c5e848a7347e7e4a2e2f4a7bc1e6e6462`

```dockerfile
```

-	Layers:
	-	`sha256:4ebb70336f76fe6eaee0b26e1b6b59d6f08885d0c27626d6c18a6031844d85a1`  
		Last Modified: Wed, 18 Sep 2024 20:58:40 GMT  
		Size: 30.3 KB (30332 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1ee3ce30618d02c39422b3a3195418083db77d3585107558576a9df2efc9f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148548530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0b1e50571d1da246fcc4535653e5a2e8ab9ac4217d9da600df1baa64c9dca6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_VERSION=27.3.0-rc.2
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD ["sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Sep 2024 16:05:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Sep 2024 16:05:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Sep 2024 16:05:47 GMT
CMD []
# Wed, 18 Sep 2024 16:05:47 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Sep 2024 16:05:47 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Sep 2024 16:05:47 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf42ea6ec4cf1c9073558af98b258cd542b42ea4f622b96e85dfd03392cac4a`  
		Last Modified: Wed, 18 Sep 2024 17:55:50 GMT  
		Size: 8.0 MB (7981913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de985b4cdcf74979d8d3c832830f8b3bd95894efdb33f21dc2d697139ec1347`  
		Last Modified: Wed, 18 Sep 2024 17:55:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a444f8ca70188a9e8c70217b108bc2e114a9176ec172fa3f95ba87f264963827`  
		Last Modified: Wed, 18 Sep 2024 17:55:50 GMT  
		Size: 17.5 MB (17514765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75756bde0387e6cce8dc7790ebb53ec0032942f2e34c35941b44aba55763759d`  
		Last Modified: Wed, 18 Sep 2024 17:55:50 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e680cec1690d355c5e2e3283b2fb97aac336deaead54847c91273d2e3ab189df`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 17.4 MB (17413837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e38ad1d2bda98e99c0b9450a439c012924d7ff9d04188001a5414fa9ed3966`  
		Last Modified: Wed, 18 Sep 2024 17:55:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a3d140f45577c41c2a781652eb827e6fe68273148dd3116c789c309c475ccd`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6945b9ecfa5213d9472fb391ad9c8ad6754c2e5bd933e0e0209e6b17a510f8cb`  
		Last Modified: Wed, 18 Sep 2024 17:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bc1b8451e7699b7bf6cbc5dd99ad111f66c5b0ec3c862a0c15716e089432b0`  
		Last Modified: Wed, 18 Sep 2024 18:56:43 GMT  
		Size: 7.0 MB (7034894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0244fc483384d0c878509e585cdf67df731dd7aa06f2639d2683452e9a004874`  
		Last Modified: Wed, 18 Sep 2024 18:56:43 GMT  
		Size: 98.7 KB (98654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c03a4be0d9dc820f81f6f8a50c7b265cedff06009aa580a4495556f8752c0`  
		Last Modified: Wed, 18 Sep 2024 18:56:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ef4d992b8c210d30a95c723fecc592c4a57b766ed5fffe94b0e88f5f137dcb`  
		Last Modified: Wed, 18 Sep 2024 18:56:44 GMT  
		Size: 53.4 MB (53428164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f790229b36677fa9d643fde4351640ab51cd2a318e0a22a33f32ac9e94de717d`  
		Last Modified: Wed, 18 Sep 2024 18:56:43 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd28f41e5c10a59139b3437921f10e8ef3478a01c1dcc127c16f70940f2537cc`  
		Last Modified: Wed, 18 Sep 2024 18:56:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c3291a0b46ebc2b09dd4b19a86d753452b57e58e15683b6e2b72c3c02be11`  
		Last Modified: Wed, 18 Sep 2024 20:58:01 GMT  
		Size: 1.0 MB (1023147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa552798d59afc7301f697d1842b620d8916891befabf30d12fc22d34e04859b`  
		Last Modified: Wed, 18 Sep 2024 20:58:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875e86a6245cb635b03406f2dae2b8ecedef25fb220f968c7e60b4926b0bfbaa`  
		Last Modified: Wed, 18 Sep 2024 20:58:01 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044095d4a221474b5c872a4129052cca9dd5eef116a9fe08cba34fd21da60aa`  
		Last Modified: Wed, 18 Sep 2024 20:58:02 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc06de34f2a463c3fd5bcb29d4184151651092978b43e68a8f2705193f3a3ff`  
		Last Modified: Wed, 18 Sep 2024 20:58:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:10f13478a4e53436e05676d289771e182e41cd010b7affec0bc9b65df357a7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09199be296411b562c2d9c5cde6f16dec9de16ca607fbb6f48394941d8ba8714`

```dockerfile
```

-	Layers:
	-	`sha256:2e7d970f4f9320e6e6a8c246cabda93856891a86d83d6723c4d79ca6a983932c`  
		Last Modified: Wed, 18 Sep 2024 20:58:01 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

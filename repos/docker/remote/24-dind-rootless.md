## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:b3f27c7b066a46022a6dbdfe676719f73da227557502f67cc5bdbdae9364066a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e1d8a8480834fce701fccce6ae088261dd1fdc9299705acddc320f7fc673b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150399717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3730c00c0a612551c4ab398a0e45fe457ce49f9142276a6d2245958e6af1dd2b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 01 Feb 2024 16:06:26 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b1f0917c81eaa7f9efb24e56605524c0f84e475e63a86b2322815479c6a252`  
		Last Modified: Wed, 12 Jun 2024 17:55:59 GMT  
		Size: 2.0 MB (2010484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92c1eddd408ecc746946b2b519ced510695ba035143c4052cb44929aa1e8af`  
		Last Modified: Wed, 12 Jun 2024 17:55:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1b2a65cdad4ed0598c893fd8d4bca6551013679e2db48368aaf9d6df45776`  
		Last Modified: Wed, 12 Jun 2024 17:55:59 GMT  
		Size: 16.4 MB (16410681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2921ea4ec3d657079f71a6c67a4c92a8b9892971355b00db4c29ff2c979f71e7`  
		Last Modified: Wed, 12 Jun 2024 17:56:00 GMT  
		Size: 18.2 MB (18177575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614abb002992071a48dc4d662e93aabb67a201b7214c79aaade87d41232df977`  
		Last Modified: Wed, 12 Jun 2024 17:56:00 GMT  
		Size: 18.8 MB (18776580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1291ed74853dc627b4a28b7288291cbf5098b194878ef666843ad5285e1c9f`  
		Last Modified: Wed, 12 Jun 2024 17:56:00 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a8215aa4896ef0012da870491106a24b1693fdf4730eae21b68457436c33f`  
		Last Modified: Wed, 12 Jun 2024 17:56:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab070e4b89730f073b675b9a66eb7a1feb9ced9b8f04881f5b4e7c6f742503ae`  
		Last Modified: Wed, 12 Jun 2024 17:56:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11aa9dfd9a28e74efcef0008b285d80aa1e5c38373a218aeaaa0bc2d6985a0a`  
		Last Modified: Wed, 12 Jun 2024 18:54:57 GMT  
		Size: 14.9 MB (14906145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d04c8331b32ad8d0eab5631d16cbd2ece5eba707a660b0d757a9117974e076`  
		Last Modified: Wed, 12 Jun 2024 18:54:57 GMT  
		Size: 89.2 KB (89185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ff23360eea1c9470ba938c53a3deba2a37c010ce8f8566e1c2100a2a80cf11`  
		Last Modified: Wed, 12 Jun 2024 18:54:57 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded06e9222aa3dfeb60ddf0323df88b09c52a35e343f549afdf34a2109a71f8`  
		Last Modified: Wed, 12 Jun 2024 18:54:58 GMT  
		Size: 54.7 MB (54740529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9463b678884abfdbdf704d25ed23b05ecb55ac4a8a7266ee878b2173bf47d1`  
		Last Modified: Wed, 12 Jun 2024 18:54:57 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ac7427a728e2f31359b9d7030696977e9841c47fb3042ecc8daeed1b14a356`  
		Last Modified: Wed, 12 Jun 2024 18:54:57 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bd974b3c8ad1ef0041ebd570dfa572355cd4b2665c1578eb66340206a559eb`  
		Last Modified: Wed, 12 Jun 2024 19:50:52 GMT  
		Size: 981.0 KB (980953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e96eabf2d4f3011dea20e9a63b15e32d665b220c5975242ce99aa378e82283e`  
		Last Modified: Wed, 12 Jun 2024 19:50:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5bbf6730f6a72a14b0ff050009823cedaeaba5238b720bbbfdb8f7a4ce05d5`  
		Last Modified: Wed, 12 Jun 2024 19:50:52 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bc7adcbf6679a84145b91e770d2f504449ba2a702d23d9f0110c6e2a28a229`  
		Last Modified: Wed, 12 Jun 2024 19:50:52 GMT  
		Size: 20.7 MB (20676182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2fdf330e3ad4a36ed3ccd75e126592d4c2c35163b810ff1a33d99eb6ab116`  
		Last Modified: Wed, 12 Jun 2024 19:50:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9f34e82e1d6ad6e3c5d99add8289559c46e2500dd623a7e20bf8fc696d65caa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b164a4e80e64d47835dfbe59bafc1f450188aaccf28f1c980c3a547cf446126c`

```dockerfile
```

-	Layers:
	-	`sha256:7e0dc375089d358d46832d1bf984c3859a36013b1fbf142b1a5a0096d12d337a`  
		Last Modified: Wed, 12 Jun 2024 19:50:52 GMT  
		Size: 30.3 KB (30274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29baa3e83bb82dacfb190ecbeba0f9271601c0149c6ce8962962dedd42a4b756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144731350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c57eb9d83a111371096535311a249738ed24dc1575b1c98dbfcfc856b12daf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 01 Feb 2024 16:06:26 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782eb4e77d74d9b9a314d9b56833c86c46848b438a32b37ea5557573243ce67`  
		Last Modified: Wed, 12 Jun 2024 18:30:18 GMT  
		Size: 2.0 MB (2006611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8746dd4cbb23fdb5e4bb3f089b9f4b73a6bd3204e0454cd67ed85adb2827ee50`  
		Last Modified: Wed, 12 Jun 2024 18:30:18 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d251f23dcd036bc3e6e8a42754613b59bd37eb5936c06882d857738b5370a210`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 15.5 MB (15459110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b347aa6775503e62c9f11acde6b8159ccda5c6324c2652b01c5fed538d98abd2`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 16.5 MB (16538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f0d74103b8922b37a8b32ca7992eae11401ccbe6c3df4e7a33321c851c5ed`  
		Last Modified: Wed, 12 Jun 2024 18:30:47 GMT  
		Size: 17.1 MB (17144869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ae2d0907a46dfa08409c9101f0edb6103164f673961ede20b345da062739b`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27298211e9a62e57bea436de1c78f6bf37f07d6b1bf6e34740a57ac3bab58f7`  
		Last Modified: Wed, 12 Jun 2024 18:30:47 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468e87477176c1ec0821b3350c6111affbeb5ef2c69ccd9456c218534d0d6009`  
		Last Modified: Wed, 12 Jun 2024 18:30:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2833bb8ce8f3cfcec0bb819590bacabc28d75d3e90249428059502445ecceabb`  
		Last Modified: Wed, 12 Jun 2024 19:54:11 GMT  
		Size: 15.8 MB (15812001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374127e549047629fa05a1b3daf0fab4fbdfe3e330fba5c6b1baec6a5dd0de0a`  
		Last Modified: Wed, 12 Jun 2024 19:54:11 GMT  
		Size: 98.6 KB (98628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fa3c2e278a048e4305947bc4a709f9a975c368db55397e90bedaeb295ffa85`  
		Last Modified: Wed, 12 Jun 2024 19:54:10 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ac91f01471a00f246e5611c261ccfc90178c1d13af15a99e6543cc16be053`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 50.1 MB (50076180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8016491d82678b83f352596f53af88ab39c7b746b79283de813b6b992505d3c`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103ca35ed5aef2cb3aeb089c775813fe30862320be8d34a4e572895a603703a9`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437b9085ed98cd25d07b8d44d0ccb4e3bf3f7f1b04453dedd5d43068a1eed64`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 1.0 MB (1023084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e085bd1343b5329aadeba463b1438ef0eb4426e18128e37664b38142e1e20bde`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba91246384a2f28b7fce8db10183b00a752e5ad7d2acbecd23de3c8c71ef8a0`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d406738ffb64ba495afd63ad263d4cd872f29086d2ec6245a8140149f806f27`  
		Last Modified: Wed, 12 Jun 2024 20:52:41 GMT  
		Size: 22.5 MB (22476094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7034c58e12ced50bdf2f0c40b4d9a1eef566d5df692b286f429d01522047af1c`  
		Last Modified: Wed, 12 Jun 2024 20:52:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:babe3c12bc10ec44c937ca38125e81d04654e74ea229ba773bf27e9bef131af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd36e7131bccad0726c4a58416aaea3a880c0c1322f06dc8ac5283e9cd99bff`

```dockerfile
```

-	Layers:
	-	`sha256:277fbb3b9248dce976f06d56c7bd5c7804877ead66ab0980cadf59f311e0d8e8`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 30.7 KB (30687 bytes)  
		MIME: application/vnd.in-toto+json

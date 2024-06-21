## `docker:dind`

```console
$ docker pull docker@sha256:03bffdab04d53ee2d34d2950f5a1bed008b5183b309e57d41244768a070da940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:ecf4ff53a1312511426b24ebe4f015a096c6d68afa5b034ced09131696142421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129957386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc751c907ca86cf0903c7a6d8946b29846021de91fd8a7fc1b72a99231c52a09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 05 Jun 2024 18:50:46 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0e9624ba6579f849b872781449af96dbbd010af575250a9a23ef5da02e12c7`  
		Last Modified: Thu, 20 Jun 2024 20:54:37 GMT  
		Size: 2.0 MB (2010474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4c96a78286d23bf9c232a4d60dcea9ff318e0077cf7dc0c7c507c1236b4ce`  
		Last Modified: Thu, 20 Jun 2024 20:54:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffee3f8ee0fd3a38e7f2b93c5c4af3b8552977e6cfe78535058d1485b62c1a4`  
		Last Modified: Thu, 20 Jun 2024 20:54:38 GMT  
		Size: 18.1 MB (18054144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ae66d00b13c9d6bca828217b54baa5431ab22bb9083fa280dd0d64332e70a2`  
		Last Modified: Thu, 20 Jun 2024 20:54:38 GMT  
		Size: 18.2 MB (18177590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64ac394bd7043f7b1807362fc3ead35a7b005e9357d373ac4d1fdfefeeadc2f`  
		Last Modified: Thu, 20 Jun 2024 20:54:39 GMT  
		Size: 18.8 MB (18776601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380426b85ac33e778840db7824cd7a6385311c3b3a8b846fdad0a92096960bab`  
		Last Modified: Thu, 20 Jun 2024 20:54:38 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dfb07abd4af6de638ab946027eb566d2b1de3dc47891904c296f51bd03fc03`  
		Last Modified: Thu, 20 Jun 2024 20:54:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74192b18fc1c8ccc38a97e527be1e5ecdfb1c07a1c501f7c132889a5dab4114`  
		Last Modified: Thu, 20 Jun 2024 20:54:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e472df9890921fa7565189c6e50ee152004db849262a7db98c38cd403fbfcb`  
		Last Modified: Thu, 20 Jun 2024 21:55:30 GMT  
		Size: 12.5 MB (12504340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf275111b412b977c58afa979020c9df84302f9c229e52b64633ab2fdd21b8f`  
		Last Modified: Thu, 20 Jun 2024 21:55:29 GMT  
		Size: 89.2 KB (89185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb552d052932a40e3cbbedb6f550b2c7b2b366d1e9910ea02edcd926af4a58d1`  
		Last Modified: Thu, 20 Jun 2024 21:55:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41173684fe28ce446dfc0a2fb0dee7de69d76d31650eb6fd73063d2f85d3fb`  
		Last Modified: Thu, 20 Jun 2024 21:55:31 GMT  
		Size: 56.7 MB (56713250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8119919d2e75f268b4ff4fc588adbbb03619dca2feb9e4f653df7dd8d93e39c9`  
		Last Modified: Thu, 20 Jun 2024 21:55:30 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf4a7532ca608560e0aa7cbcc6625774d180aeafec78803788c818ce277d77`  
		Last Modified: Thu, 20 Jun 2024 21:55:30 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:747f493e06af877fdb40aef361ee2df73c2c20a0b60c21522073094235c16856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb092c29c01bc40985305caa33d4d4ae9d61f651e8599df1f29833369d7805ce`

```dockerfile
```

-	Layers:
	-	`sha256:0b2d66df662b58a03250de6c2f4cb0b2d1d4a6827066d55789995cb064e520c6`  
		Last Modified: Thu, 20 Jun 2024 21:55:29 GMT  
		Size: 34.5 KB (34522 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:5125e5c0e9b0f86c5f0cdbe528707a2e32d2997720cd8a8b7880d50a28a9ca65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124394160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896065b4962c6f50ff1ae5ac560b7970426190193b09bbfc584c2935b78f0989`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc3921df5257d82d5f947c4026d8074af5c4d7e9307f821fe12ed84d11dbd5`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 2.0 MB (1993321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a779dee551fffb6e92da0afeaa8132f89aeee927cee10dfb3bd0648e29db439`  
		Last Modified: Wed, 12 Jun 2024 17:55:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50776b5a8e1f28d4c15cf5bcbc61cc19e56da3909b3e4547b049e10e0391a88c`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 16.3 MB (16329503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057d99de6d2589b2c0b039447ad492fc9c3856ffd0a6f93f4731b579e2238a5d`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 17.0 MB (17010710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c074d89e837f491eab5ad89463383211d1e1f049fe60a8901fdf502326098`  
		Last Modified: Wed, 12 Jun 2024 17:55:47 GMT  
		Size: 17.7 MB (17738761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398c270a05c2e866f342c5cfe5092595dc35d0d2496ae46ed15bbbf34a77cea`  
		Last Modified: Wed, 12 Jun 2024 17:55:47 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2d42bf1d9a1cd7b505502944d46f78be91257f7137304ccc2ebcfddc0aea39`  
		Last Modified: Wed, 12 Jun 2024 17:55:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2da79cf56c3cffc1cd42dedda8f16eca3c493c273c9be2d6f91d12f4165da`  
		Last Modified: Wed, 12 Jun 2024 17:55:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5658654a6550f3588597abfbdd4694153499e490f0434c4265a4d0e7e0d824e`  
		Last Modified: Wed, 12 Jun 2024 18:54:53 GMT  
		Size: 14.9 MB (14858358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951c19626eaa9b24c96bac33e217f93e1c18f6a581b5834dc2c4a010b8c07901`  
		Last Modified: Wed, 12 Jun 2024 18:54:52 GMT  
		Size: 88.4 KB (88390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267d544f34ced5c78f9719e88509e98ef232c7fd087818851749a8161f2f0d5a`  
		Last Modified: Wed, 12 Jun 2024 18:54:52 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b8590917403fb79517ef7e9f05725660dbb258154c99a3d2fa661a013e0d86`  
		Last Modified: Wed, 12 Jun 2024 18:54:55 GMT  
		Size: 53.0 MB (53002100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2553cf1092f5906b26205a1b0a80bac83625437e21d258177b7b7264483eb923`  
		Last Modified: Wed, 12 Jun 2024 18:54:53 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe71747c2c8e828b1fa2e3546e920b31396ce6da26c7f48c49ee515f2d2f095`  
		Last Modified: Wed, 12 Jun 2024 18:54:53 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0eacdce475cd570f936677a5239cdafca55888efb68a2f589f59c3179bb9fae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b309d50eeae382fdac4589cd4277f02e138fbafead972338bb0599233459515`

```dockerfile
```

-	Layers:
	-	`sha256:539a2eff542bdcc7ed43e04abd574cf103c45efac8b766586f167f9419bd44df`  
		Last Modified: Wed, 12 Jun 2024 18:54:51 GMT  
		Size: 34.7 KB (34740 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:72b08c0e4b4804143be1816a4fecb62ed37a159f1c2d90e8d92cd4817db650c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122586386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c50e337eca472a3ea2791169c203de906a354a942945d46afc320dfcd66e94`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4176f76244fd438271e663ab7a8dda92f04446dfdc569bef106849aa6b3290`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 1.8 MB (1841233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a779dee551fffb6e92da0afeaa8132f89aeee927cee10dfb3bd0648e29db439`  
		Last Modified: Wed, 12 Jun 2024 17:55:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ad1c5f9aa601849dcf4239cfea69887a950238038a49dad97ff1cebd10dc23`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 16.3 MB (16319680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940bca3c709c27f0eb1a1f2ab8fce0bd22f6fe7241dcce407a6f0d3bd154004d`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 17.0 MB (16995852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a8468bbabf8fa9eb9f9d16b23330947edd3b32f22196334ca17e6512688e50`  
		Last Modified: Wed, 12 Jun 2024 17:55:47 GMT  
		Size: 17.7 MB (17720932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc49f5408c403177b1ce4a9bdfe8095721fc65ff734b59c7cb6919583a2d6c9`  
		Last Modified: Wed, 12 Jun 2024 17:55:47 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2a854c36a6bcbbad6b323d149ca949a3ee9c3968b64b406f15ee4912a792c`  
		Last Modified: Wed, 12 Jun 2024 17:55:48 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2da79cf56c3cffc1cd42dedda8f16eca3c493c273c9be2d6f91d12f4165da`  
		Last Modified: Wed, 12 Jun 2024 17:55:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc605c910d5d6b92e6e20540e7ae11ded32e794e738f2031ef147e1282e1df5`  
		Last Modified: Wed, 12 Jun 2024 19:00:33 GMT  
		Size: 13.5 MB (13520104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac8e5974d064f4c743cfb0a11ae1cec4883201201f99bc653aaf2308563669`  
		Last Modified: Wed, 12 Jun 2024 19:00:33 GMT  
		Size: 84.5 KB (84464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83c232e121fe324acb278bd7224ce1359b362752722f7e6104bf9c8ccc6ec23`  
		Last Modified: Wed, 12 Jun 2024 19:00:33 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47815fd8aee5451df118c3251082a6380362979d6faa626796f63877956d0a5b`  
		Last Modified: Wed, 12 Jun 2024 19:00:35 GMT  
		Size: 53.0 MB (53002123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15125b524b7f0699e80e2c214ced10299dbe212007f749ab14dd8e6bf890ec4`  
		Last Modified: Wed, 12 Jun 2024 19:00:34 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8cf0bf35dc27a002985fff298fa5751109d5d2dc7ae8ed278f8c2f0388e389`  
		Last Modified: Wed, 12 Jun 2024 19:00:34 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:29840c20e16e09d558cd1be6ff1a862594017108258cdbd3b522f454c983101c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd21f827b096ca55a5b36ef7127296118d771d861b882a1b8dfbce079b087915`

```dockerfile
```

-	Layers:
	-	`sha256:09060292673a77cedef11d79fcde917112c7c3d6dc40c1650c9362dab1e7fd3d`  
		Last Modified: Wed, 12 Jun 2024 19:00:32 GMT  
		Size: 34.7 KB (34740 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c57e6ab412ce8e05f6c40df6ca6a79d34ca8e5ce51c1f308ff578ec9d6694d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125025806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3ccd246fc282b89b24dc24b4cc90f60bcfe966bd308fca488fe91a1bfac00c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b25ed5893174a51146879f720bd354232af48e27095ddbfec03a7659109ec`  
		Last Modified: Wed, 12 Jun 2024 18:28:55 GMT  
		Size: 2.0 MB (2006608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0285b845bf0c704809c17ad3ebf8b54d6b4d0f9a42085dd399f228e3e8fb30aa`  
		Last Modified: Wed, 12 Jun 2024 18:28:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3652bee2cc07f872b1544680426d8a307780628f71e096465ab58e96f133b4b6`  
		Last Modified: Wed, 12 Jun 2024 18:28:55 GMT  
		Size: 17.0 MB (17011545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750e37de6bad65bfb38f247ebda26c0c889ac54905e1061d2895cfe3eb17a479`  
		Last Modified: Wed, 12 Jun 2024 18:28:55 GMT  
		Size: 16.5 MB (16538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afdd4eb6a89f1b9ca693ba0d3167c792b212eded8f77b0c88869c2d671f8235`  
		Last Modified: Wed, 12 Jun 2024 18:28:56 GMT  
		Size: 17.1 MB (17144856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec087a23b5291b09dd939713cc6407e2e6ac0b16d75924354aeef52018fce33`  
		Last Modified: Wed, 12 Jun 2024 18:28:56 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfa1a73ef0186b089fd24722e5e31d3f368a0e66e1ebf73eb13551efd8c51d4`  
		Last Modified: Wed, 12 Jun 2024 18:28:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6602da43e395ffe8d3b753e8fa989a616089720c01dbf5aefe37b275d86d5ea0`  
		Last Modified: Wed, 12 Jun 2024 18:28:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2943ff8056330c0aad2b0a1861486ca0ca4dcfba101ecf111996668571fb724`  
		Last Modified: Wed, 12 Jun 2024 19:53:04 GMT  
		Size: 15.8 MB (15812089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504c505cd5434eb129595585c8f1d8a4259065d4641539f9f30ddd89c9170694`  
		Last Modified: Wed, 12 Jun 2024 19:53:04 GMT  
		Size: 98.6 KB (98624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551a8405f1508454a45427a14f710969dafd44cacb6fcd1a007bf18a4a26304e`  
		Last Modified: Wed, 12 Jun 2024 19:53:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abd3dc56e5fa9a16c02443ad479a375350d5606f7c499c1435989b4749001e8`  
		Last Modified: Wed, 12 Jun 2024 19:53:05 GMT  
		Size: 52.3 MB (52318671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed5aeee147f05d15c357bb515ae3f56916b5dab26867954f94e8d66144b48c`  
		Last Modified: Wed, 12 Jun 2024 19:53:05 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c948c9193623f822e64e45a83538dfe9eb73fd9f49087f3c0a460314bf6735e`  
		Last Modified: Wed, 12 Jun 2024 19:53:05 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ff5da99670c49f0d2e85a5e7d40f312e6c14bbe198409146d46d39cdc6448e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbacf6137d9a9f8f3ed0bedaafe09061cfe9efe386227b0047360da0d3fcc283`

```dockerfile
```

-	Layers:
	-	`sha256:2d66136ef659d0370d3fd17ab6eef284d5c51c247ef994b99c8af7ad78847d54`  
		Last Modified: Wed, 12 Jun 2024 19:53:03 GMT  
		Size: 35.0 KB (35021 bytes)  
		MIME: application/vnd.in-toto+json

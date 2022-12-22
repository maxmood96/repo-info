## `docker:20-git`

```console
$ docker pull docker@sha256:1a908113501ee8418173ffebc883f1211ed415bb47c695c7a65a4a3fda3d77e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:99d0c2c80b9df74795d5b1549ff2b33b4e7e3f68531305b6041c981200582b47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53240143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285dacd2c10c6b3cb836e979201acbf937478935552697d49d98819235824fc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:27:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:27:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 16 Dec 2022 23:19:56 GMT
ENV DOCKER_VERSION=20.10.22
# Fri, 16 Dec 2022 23:19:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 16 Dec 2022 23:19:59 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 16 Dec 2022 23:20:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 22 Dec 2022 01:56:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.2
# Thu, 22 Dec 2022 01:56:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-x86_64'; 			sha256='d056a8330a01f22c249b9fa03ad0d5be889b79b648cad43c8549eb4c3f8ff0ba'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv6'; 			sha256='164b04d5970f340eb6cb4da171b2dc0d12c345a6092c8ac2409b5fb4fc8af5e6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv7'; 			sha256='6e01028d97bc48bfd3894d9161586e74c0f37cf7d67a67ab7eafb351c2003cb3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-aarch64'; 			sha256='48ef22ecea70b4b197def1c1bfd2e797f7117db5257f6e505e64f03fdc329a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-ppc64le'; 			sha256='8cbceb45fc656ec9f9e24b8e61fda54d233ecc8f46cee8ef5ae5acfdcc7940d4'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-riscv64'; 			sha256='e9d612ff8d198911f93706f4eec2bb58abb24c0f869cff7d69f6a8e24ce05420'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-s390x'; 			sha256='9fec4a8628729766f4600ec0f8fb5aa760b6a20673e1abfb3d78f3b2eb02696a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 22 Dec 2022 01:56:40 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 22 Dec 2022 01:56:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 22 Dec 2022 01:56:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 22 Dec 2022 01:56:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 22 Dec 2022 01:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 01:56:41 GMT
CMD ["sh"]
# Thu, 22 Dec 2022 01:57:04 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eea1d5d8e5eb7f3c01c44eb6652605d4b5ad66cf819d1e3b6053733f2f13cf`  
		Last Modified: Tue, 29 Nov 2022 01:28:59 GMT  
		Size: 2.1 MB (2064254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41ddca615c02560ac2876c1f1a4f4f0c2fe3f8b091488146e1098c5a3eda4`  
		Last Modified: Fri, 16 Dec 2022 23:22:29 GMT  
		Size: 14.0 MB (13982924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76f94013e41735f015f26d3c3df1af256e1fd761926325deaf30759c53494`  
		Last Modified: Fri, 16 Dec 2022 23:22:28 GMT  
		Size: 15.2 MB (15204113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36812387b4c0b6952d3037454b2c7d02ccbbbaccb9056155a2ed8962434c145f`  
		Last Modified: Thu, 22 Dec 2022 01:59:05 GMT  
		Size: 14.5 MB (14474966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7e843175d06d19e47a3cac2e4df9ea9f20e3762b5006548b6db1ef455ba153`  
		Last Modified: Thu, 22 Dec 2022 01:59:03 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f70019cf2a12746bc56dbd4b414fd3da476a518f99f58eb66c678c5832cfda`  
		Last Modified: Thu, 22 Dec 2022 01:59:03 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a00b8fabf3f9d11aee43b8d6a0470679d58fa1a993cd00f0013a42e6bec402`  
		Last Modified: Thu, 22 Dec 2022 01:59:03 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6da47cc3f0c9c55616896eb6802c2890cecddbda22d3670032a90a99602eb0`  
		Last Modified: Thu, 22 Dec 2022 02:00:21 GMT  
		Size: 4.1 MB (4141451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0163c4e664e1a8c4775fb06c645c51a4aa0656fbfc1e83299492e3551cbd803a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49053824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedb1d205098201a35a59a23e762f79fa84e00a5600e18aa76e8fdba562a1d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:42:08 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:42:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 17 Dec 2022 00:10:28 GMT
ENV DOCKER_VERSION=20.10.22
# Sat, 17 Dec 2022 00:10:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Sat, 17 Dec 2022 00:10:31 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Sat, 17 Dec 2022 00:10:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 22 Dec 2022 00:42:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.2
# Thu, 22 Dec 2022 00:42:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-x86_64'; 			sha256='d056a8330a01f22c249b9fa03ad0d5be889b79b648cad43c8549eb4c3f8ff0ba'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv6'; 			sha256='164b04d5970f340eb6cb4da171b2dc0d12c345a6092c8ac2409b5fb4fc8af5e6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv7'; 			sha256='6e01028d97bc48bfd3894d9161586e74c0f37cf7d67a67ab7eafb351c2003cb3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-aarch64'; 			sha256='48ef22ecea70b4b197def1c1bfd2e797f7117db5257f6e505e64f03fdc329a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-ppc64le'; 			sha256='8cbceb45fc656ec9f9e24b8e61fda54d233ecc8f46cee8ef5ae5acfdcc7940d4'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-riscv64'; 			sha256='e9d612ff8d198911f93706f4eec2bb58abb24c0f869cff7d69f6a8e24ce05420'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-s390x'; 			sha256='9fec4a8628729766f4600ec0f8fb5aa760b6a20673e1abfb3d78f3b2eb02696a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 22 Dec 2022 00:42:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 22 Dec 2022 00:42:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 22 Dec 2022 00:42:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 22 Dec 2022 00:42:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 22 Dec 2022 00:42:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 00:42:24 GMT
CMD ["sh"]
# Thu, 22 Dec 2022 00:42:44 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5dec0c1f562bd55dc773ccc0c77fbfd42b92083262478523c19bcc0f397af`  
		Last Modified: Tue, 29 Nov 2022 01:44:14 GMT  
		Size: 2.0 MB (2036851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9db874a82a64c48213d6d1ce2e45eb51359f913358fa4d785dd4a6d5219631c`  
		Last Modified: Sat, 17 Dec 2022 00:12:52 GMT  
		Size: 12.7 MB (12743372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcbc5124e189b1ab3f0affe49da5b5b8037788919a0816840b1270409f1a3c`  
		Last Modified: Sat, 17 Dec 2022 00:12:50 GMT  
		Size: 13.8 MB (13764588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572c6a0495bae03ba20f90613abc188cad665013e35020ba40543ffac50acfb5`  
		Last Modified: Thu, 22 Dec 2022 00:44:41 GMT  
		Size: 13.1 MB (13063326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022b5312edccca9a4c10eb4e85ca00d45828210272545fa7f62ddc75df8e7d80`  
		Last Modified: Thu, 22 Dec 2022 00:44:39 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eb3085741a5e382a2678a3d485bc0d0912b6de55ebde075a9dd0c65bf107ca`  
		Last Modified: Thu, 22 Dec 2022 00:44:39 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed99cff288a78915b73a655cee5ad15234a3439368e492a3e22a88ac5cd54756`  
		Last Modified: Thu, 22 Dec 2022 00:44:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da3263994956662aa919ac9698e66303fe6c7ed98dcc0c3c6d92eb313ccadd`  
		Last Modified: Thu, 22 Dec 2022 00:45:49 GMT  
		Size: 4.2 MB (4184771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:25-cli`

```console
$ docker pull docker@sha256:8d8b1ec7c0da9bd27e28e73f68f798890f217deb9a0595f7de274126fd8b3fdc
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

### `docker:25-cli` - linux; amd64

```console
$ docker pull docker@sha256:72f73e066e5643801975099020ca08ce6bf282d8d7e9a976e95db3e40dbe0f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65618730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec40dba20efcdfc4ba2443fcacd8ceffd0927de076112477ce2d300425bbc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Jul 2024 22:06:10 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["/bin/sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Jul 2024 22:06:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7679290b41e2c048913474cf0c2e5caeec6ad666e9e0c95a5bc085f1e72d41`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 7.9 MB (7869178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed5af691a7bab21d5f072ee2359c6f5f3845dfaab1820f84ebf5627349c634`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e00f7927455cb1e16403bfbd1f1ba6012145c6ad1951b673f7df9c7fc001d5`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 16.9 MB (16902830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afe6918934a3143d63818f73f2938c7a0e9ff9d1092103fc5d28e6425382ba`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 18.4 MB (18404714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728a4abb38a87c59f46cca8005cf22c072ada1076ce10c76718359c666702856`  
		Last Modified: Mon, 22 Jul 2024 23:03:25 GMT  
		Size: 18.8 MB (18816965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc39c5a0e612118a688cce82addbc8dd2ef956f7a3534d939ee237eb0ac70ae1`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a90873a8c93cb7ee93115481a37fc5fe72f772ec7069539c41c8de58d5f74aa`  
		Last Modified: Mon, 22 Jul 2024 23:03:25 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490c6db84f5f31a63ec6e2dd6342a7c1f9c633e7681858278c783153316dd7f`  
		Last Modified: Mon, 22 Jul 2024 23:03:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:99be3567aa2c7f8c5bffc30c54a5c29f7569b6501239477e80df3438fa4390fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78b0a500d61290fc6b3fba2b72edd200a712972d55b1c7a5e8d8a9a49dfc993`

```dockerfile
```

-	Layers:
	-	`sha256:25b2cbc338bd72dd9e8c522621609b1517f66d1cf63465418392e09733292d5d`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 37.6 KB (37622 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:28587c422c02ea3991bef576fbb57e13c66f366f863206d0b438eccc5f93343e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61331635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d472bf92181f3fc7999269a110aaead0748df6e15a953a08461426e55dcf453`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Jul 2024 22:06:10 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["/bin/sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Jul 2024 22:06:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acceb8f7b1778b053c01711ea320058d1fa30ea253a82a8f9e4279439f2671e5`  
		Last Modified: Tue, 23 Jul 2024 02:46:51 GMT  
		Size: 7.8 MB (7799501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ceaa340dd91ca232b4309a1884ef59234cf953c0edc16a6f59c76eb6b27ab8`  
		Last Modified: Tue, 23 Jul 2024 02:46:51 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a5d61a45186f20687503ab9967c7613d0cc0e7cc44a54c76ee2c0e962a3624`  
		Last Modified: Tue, 23 Jul 2024 02:47:52 GMT  
		Size: 15.3 MB (15274082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec41c43c1930ae29758edc291d189cf843dc646558f9bf35224225748b447d4`  
		Last Modified: Tue, 23 Jul 2024 02:47:52 GMT  
		Size: 17.1 MB (17117259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb33dce870cc6b531c381e343aab5308e7a6fbe74f80f85f09fb8338bad23fe2`  
		Last Modified: Tue, 23 Jul 2024 02:47:52 GMT  
		Size: 17.8 MB (17773459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b880e8766c93665444af5260e35d1fb19dc11dd69b2b34942c4f67b51ee8c75d`  
		Last Modified: Tue, 23 Jul 2024 02:47:51 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181f9f9c9e3815c27db57ca1467f477e0cdbd85af33c7727e953e96b906ee80`  
		Last Modified: Tue, 23 Jul 2024 02:47:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107a99db32c6dbad37a5d90405ed75953a7d9e20aef978eca8f6a71272f35730`  
		Last Modified: Tue, 23 Jul 2024 02:47:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:33f2a461db219305d6aac90f28cc2c6d6798e6080f5263d035f9f224a1b5426a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b7d1a2cafbed169cce76d623ddfb5d93e089fae5464853a1b2c4bf208576ad`

```dockerfile
```

-	Layers:
	-	`sha256:70121916d03143b6e535b1659dd02921bffce4e6d0fe2b0330cf993a86e228ea`  
		Last Modified: Tue, 23 Jul 2024 02:47:51 GMT  
		Size: 37.8 KB (37771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:120743988a1bbf34b3d0183ba1be512c6a041430295029db060c7081c9523713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60374245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7110a7f957ea5253c56bab9fbea360867584435d94d58f379c22a14d95ada1be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Jul 2024 22:06:10 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["/bin/sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Jul 2024 22:06:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965a161b46eebc9386e4cc59dd83c8eceac1fd13be3e5f3e064c8b9e32e44f33`  
		Last Modified: Tue, 23 Jul 2024 12:13:50 GMT  
		Size: 7.1 MB (7138056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b987ba0b4df3b36b9fa3aa898dc1f8aefdd672399f7f1375e293e1e757799174`  
		Last Modified: Tue, 23 Jul 2024 12:13:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebfe65db0fa27340c27e799cb73671316ffb668664f7d04e0e6e846efecf84b`  
		Last Modified: Tue, 23 Jul 2024 12:16:28 GMT  
		Size: 15.3 MB (15273174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be09b9f103f47c0982873eed5f5af784bb169d4b642bb024d85a05eb608ce88`  
		Last Modified: Tue, 23 Jul 2024 12:16:28 GMT  
		Size: 17.1 MB (17104848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad1608991747d3127f75b63134afa00a4513f9e61a8ba7f2069b12614162b05`  
		Last Modified: Tue, 23 Jul 2024 12:16:28 GMT  
		Size: 17.8 MB (17761050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d26589fcf5486d459777e81ec86fa22d4db2bd992c4eb436124c9f8ecf44cd`  
		Last Modified: Tue, 23 Jul 2024 12:16:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b4640875707df3424150b20617efe427b0db6ffd67f2a5286ad6efe4f71841`  
		Last Modified: Tue, 23 Jul 2024 12:16:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c256c4b81688b19e9af11e93bc6e0440d3dd9b529a5a44e591ed786cc5a2be5`  
		Last Modified: Tue, 23 Jul 2024 12:16:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0a5f3a85c6d69ca3fb8ae68fd0a68b0ef883e2e94e0e49096fb595e04d95cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fecbbe44394d2bb01b14e2cb6c5025f7aec08cd71df62b5af0e12571e66e66`

```dockerfile
```

-	Layers:
	-	`sha256:6624359259416f6eecf1796bf6b5c41838b046e935c450e3dfbdcff9dd9b24d6`  
		Last Modified: Tue, 23 Jul 2024 12:16:27 GMT  
		Size: 37.8 KB (37771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:171f355694307a49aebf7fe26f4a3897ec4ac7a8ef5916f815cb630260bcc669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61919850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aba1155891626405f8dd73ab56a313f6a3aa8d2564d6cd4d0d637be3fa7ca52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Jul 2024 22:06:10 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["/bin/sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 18 Jul 2024 22:06:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Jul 2024 22:06:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Jul 2024 22:06:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 22:06:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd8e63efb573ee2b0f35dca00f28c63ee581677459c750e4526a3bbfef083b9`  
		Last Modified: Tue, 23 Jul 2024 13:32:35 GMT  
		Size: 8.0 MB (7974622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb696accb71220e138bae937340d074366c0c142479aa5308441332c88954dd7`  
		Last Modified: Tue, 23 Jul 2024 13:32:34 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e14aa9aa6c9bc2c4221b3c362dc79f6124786a071dfbfab4c1f7b001309abc`  
		Last Modified: Tue, 23 Jul 2024 13:32:35 GMT  
		Size: 15.9 MB (15907332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b210fc3a48deee560b7e7064245c866955f57340cd8d9eded134e67cdd818c50`  
		Last Modified: Tue, 23 Jul 2024 13:32:35 GMT  
		Size: 16.8 MB (16772763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ac88b1b838fef2d70f3b2b6756b31df5cd2185a959ba6321e79f5ebe2b55d`  
		Last Modified: Tue, 23 Jul 2024 13:32:36 GMT  
		Size: 17.2 MB (17176047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef9703ec561bbe82e34e3008664b0646f2697985d89c2b38d67a0f3400108c4`  
		Last Modified: Tue, 23 Jul 2024 13:32:36 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c33444b11ab6e54b80a010f46f685992551f30fb4471db4d6fefd6fc5dacb9`  
		Last Modified: Tue, 23 Jul 2024 13:32:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219b6aa55da4c4212af272ac78d727f65d167e56e7829244c07a069f70a162f2`  
		Last Modified: Tue, 23 Jul 2024 13:32:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d50b93ca2b96f97efb80044698f072c8bdeceb89339fe1a8f701404cd895d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7638b184d2657396ec6aa9e3702ec324e801a170ba40f548b1a2d9b797d66a`

```dockerfile
```

-	Layers:
	-	`sha256:e7f6b32d98f425f0f928e6d7f9126ffaab7ce0594bb4bf86440f044f8e87ddfd`  
		Last Modified: Tue, 23 Jul 2024 13:32:34 GMT  
		Size: 37.9 KB (37922 bytes)  
		MIME: application/vnd.in-toto+json

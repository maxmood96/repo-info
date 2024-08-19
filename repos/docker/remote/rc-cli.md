## `docker:rc-cli`

```console
$ docker pull docker@sha256:81048ed8334a2d2e2b2be95a453b66dafd5e8ab95df98538bd464cc51355e973
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

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:1fa51c3af005f21023d1d4fac4fd5731b2d14ef1afc5dfc4ead0da31b9aabd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67045626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfec9bb775d05aabce0d60e0921dbffc97bdc14cbd5b7f8ea9afc974f87a97e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b826b4df39e8b6818aebd9eb70c4704bb0c97fc2cb464aa28510da90630351`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 7.9 MB (7872281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ee97e7ed5f9f5b0e8abbbf4bd025bff9b040451692c8c646b6f6acc5a1270`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb812271b283b43e9c4f2f97567fef7a516fb56c9711dfc83c2d1542037c468`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.3 MB (18318205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b789603700e5b3db4e3d0433d1a05227e1bc914313dace943393a7ec2388f45`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.4 MB (18404803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3295e68d9ed551c77c847e1464219797b4f10b538bd1d3ddb7845d83adf451`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.8 MB (18825286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9917b18cd48d8e82e1f25127437de1b1c380fffd40cce7476361dfbdc7a73202`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6acf233fd00d766253e3e1a75561098dd84c85485a3014718c78820e1c0db6b`  
		Last Modified: Mon, 19 Aug 2024 18:59:21 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7925fadc402ad01d5de8aaaf5e54e7255a07c6bd6a36565c4bec0eaf098f49`  
		Last Modified: Mon, 19 Aug 2024 18:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f07c6ce496dcace0a0062d7476bdef131f008c54811b9c3ce87129d96b38d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63195544cfe5910b5647e3a77f6cc31bedf524aa40de7d2533a8c1122110c924`

```dockerfile
```

-	Layers:
	-	`sha256:37f9232abcd3d092ad62525211f1acc319c30f1f921477dced976208664cf8ee`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 37.7 KB (37710 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ec5d35d882e59a2515e9891a9144a85b3e3985f7c59b6d612b0784eb1b26a2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62650142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0188fd60a5144f0b16ef1911ac8e781d8f7f17101fd97e7d527429504203afc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cd7328f0b7553023390e36003472a46b8544f5d0208826dbfa8cea0ab75584`  
		Last Modified: Mon, 19 Aug 2024 18:59:16 GMT  
		Size: 16.6 MB (16577294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0780943347b16a7fa280637ea799b2f561ac9fa59121f4a69f346891128efc7`  
		Last Modified: Mon, 19 Aug 2024 18:59:17 GMT  
		Size: 17.1 MB (17114708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f449495d35e9274c80420f20fcc7f50b96788297b1d55a43ecaee92b7b9c`  
		Last Modified: Mon, 19 Aug 2024 18:59:16 GMT  
		Size: 17.8 MB (17783301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516d8517fdcc75f25abf282854de05e764bbf1b80bf3676926e4369d8659c54`  
		Last Modified: Mon, 19 Aug 2024 18:59:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f7fd32c162a1c5fa97cffdae6f51761b1f9d6a2aed1601d4a537ea19edf8ac`  
		Last Modified: Mon, 19 Aug 2024 18:59:17 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f8030f3ff465acb9510e41c77bf5362b3643c069229760a246a061b9b7d6e`  
		Last Modified: Mon, 19 Aug 2024 18:59:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23e416a7ec014bd46706e2e7ebc18d1532c1606de12d7c30355810b9a3c996b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855f1e4cc07f2499556a71205bbfeb75a42d31e23561f8ef45e4badbeeba0dc5`

```dockerfile
```

-	Layers:
	-	`sha256:e22edba1ba69dd816dd9bc8ca2220e002e6bd77949a5161eeb38cadd0a482304`  
		Last Modified: Mon, 19 Aug 2024 18:59:15 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb31277f32d0fb369afec2413955658a251e0068d3384846f8b5079575983a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56010545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bc13d7ae71ea20eb9790e20167611b15cf2a42ee55d1a0bcd205ddc03628c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 17:10:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
ENV DOCKER_VERSION=27.0.1-rc.1
# Fri, 21 Jun 2024 17:10:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 21 Jun 2024 17:10:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.0
# Fri, 21 Jun 2024 17:10:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-x86_64'; 			sha256='359043c2336e243662d7038c3edfeadcd5b9fc28dabe6973dbaecf48c0c1f967'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv6'; 			sha256='398d717e6cc9515ca0325035cfe626cbaaa1023754cfd22c13eab6b29ecc2d54'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv7'; 			sha256='604c00f22176ca8291f43d22f066cfcc89f4c09de2113d287f72c0bdcf611e46'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-aarch64'; 			sha256='296076f4d14d2a816ad750f6890355fc118692814e4b4542942794817f869d37'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-ppc64le'; 			sha256='c88c097fa475f07140c01e3ca370a503b927f377f200114fa17e0bee6e0cbc4d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-riscv64'; 			sha256='b563b99c5a1c03a1a83cb56ea1f7a492ef74e137afd0cbea485b828b6c61dbe5'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-s390x'; 			sha256='f701bd64dc5b204352c788931b43de9c778d47eed1be7caa81b57fc47a09164d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Jun 2024 17:10:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Jun 2024 17:10:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 17:10:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3be0ff3f8430a7c5e4c0602a3a190116b4a4d4d1d16b89c627d5436d8d3318a`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 1.8 MB (1841225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e90c200cd38a52aed6f4457d4fb93031e32aab75a2c05019a3a2dda9db6b7f`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb755fd46ba8be39c37074bdc8778c82778acdb1af8434d1404456166132219f`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 16.3 MB (16336726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24f5075d7a1c1c966789cfd6c0a00ec11d9ec063c0d23d09adcd6808b8b1a4`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 17.0 MB (16998029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9e479a6f88b8467dd8cfc0675ade5241e4cc443db9b52234334ac885ff280f`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 17.7 MB (17737536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eab426e7ce487450b94b7007d5078b2083e2d671d5d781b6ed55b8046538a9b`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dd28ce1af5a7c84e79f474ba29edaa351ab049bad9d407ff4b89f021d6dd37`  
		Last Modified: Mon, 24 Jun 2024 16:53:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb73e169e1e66eb6716a44e3d4c680696f43c52dbfd6e656b9346f7ed9d4d51f`  
		Last Modified: Mon, 24 Jun 2024 16:53:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:efcd61aea732a092f6ca8485520165f724eda56200ae6914e6b07aa5cf441096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99a14dc613df1c0a715b136cbbba010bc38f2c6ffcdf35c92d356e7cd0fb524`

```dockerfile
```

-	Layers:
	-	`sha256:7f13571a1739a7687399f7ca2055c21a65243cf9f40d6ae751ab4f5de533d076`  
		Last Modified: Mon, 24 Jun 2024 16:53:23 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a7395aa6fab4c1a24a3a192e9ee84f842a5eaa49b560097db8db29d754ad77ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63295507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de6eae0ce59d5abca4886b66f9daa4c16e192f19ddabebb9bceaa4f2d0be73b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19dc33df4c8f435b82bd76228e820d17db82bafa51365d6d7ca39f18b0ac35`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 8.0 MB (7981766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc98e249bb1c68fcd6c7af4cd94d4dc840949342f303f3453b89e47b10baac`  
		Last Modified: Mon, 19 Aug 2024 18:59:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b064ad1c39cab9bbd12ce8a44da8ca317ae42aafc3a703eb68481279fac32d9`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 17.3 MB (17264856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36074db9005cb79314791a9d04733048d5cb0703a7ac13b89c26d810045b89d`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb8b806a016e2bd5e83e137c7787981575ad2ce863d92ce07cee3fc38544c78`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764856852ab1b254b572502db9ed0d8fd601e8e615ae83ba73c5a1e5b592c9ab`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d43f3808e72acbc083572802b4b53a88aa4088c8e2d99825cef40e03c050fd`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12ab67b46ae8edc30d74e102545f60cf7042a2542f02c2b8e7f0a313592f473`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e10f2c6fd467d145de4d4a14fa8ca75a1ee80fe11c0d42eb6e323b5f743df97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fd9030e8a86dd7741b31e53d376214fbd782a1e59b457e75334c2d9aab2c46`

```dockerfile
```

-	Layers:
	-	`sha256:17b7467f3e146fec54cae7f008e9cf996f4c6289eb67a6ed6f3507501ea67e9f`  
		Last Modified: Mon, 19 Aug 2024 18:59:39 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json

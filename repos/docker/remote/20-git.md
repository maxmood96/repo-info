## `docker:20-git`

```console
$ docker pull docker@sha256:28e473065b42f54ecfccc0d84777a16e971ab628523736f24bb6e3b83c34890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:65a46b762db55ebc894b9f2d25114565c4435ee7c3d2433948ac7e5f2a12678c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80948983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec20857e2d493719cde04da6183d772d4af62f77e58be13fa9f2da7b0410fdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:04 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 14:00:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:11 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:12 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:13 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:38 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725c26e6c961574bf4f3724a00437531fe5516503dea1a400472aaab84aa04b`  
		Last Modified: Thu, 01 Apr 2021 14:02:01 GMT  
		Size: 69.7 MB (69692145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6f85a137108b8770a52db03fd0fd44a040154d6fcdec924b5a35a809ddcbc`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e76fe2b4373aec860cb8939d340af3ae94fdc318eedf36a3721cfb1bf7c20`  
		Last Modified: Thu, 01 Apr 2021 14:01:48 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bb38bf23d36b2dd31bb0d551d5ccfd0a39ad22ff52a12fd1ab2bfa69f66db`  
		Last Modified: Thu, 01 Apr 2021 14:01:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200f3f4a506a8bf68892a66feb9d023930b3e910b62baaae5fcfb942c7bf3d55`  
		Last Modified: Thu, 01 Apr 2021 14:03:11 GMT  
		Size: 6.4 MB (6392832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a8ca53682290cf0a342ef42f5458905385619e2099e34d67959d842426ddcd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75024239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf59598d54119927f27ec71c136d3a901fbff352fd5f2b560a28c00bd4972a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:18:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 13:18:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:18:41 GMT
ENV DOCKER_VERSION=20.10.5
# Thu, 01 Apr 2021 13:18:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.5.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 13:18:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 13:18:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 13:18:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 13:18:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 13:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:18:57 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 13:19:34 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ae8fa0eec8970b4efc19ad3bb6efe75da4ba6c2484d6104ac8a5d4dcefa5b`  
		Last Modified: Thu, 01 Apr 2021 13:21:00 GMT  
		Size: 2.1 MB (2057878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf55a957502d5c4265115c7d959e01b52552b726fd320db2b0bab15365f0069`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b6b0e45391ddf63837646cdc3ed7eca01744be743ef2f2bfc0f464a24da6c0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 63.8 MB (63776788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b0590ed030ca2477043adb258f84eefe2196e41175fb86d9d79ea7b4f99cc`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b14f5baa86ccb716099e65f62cc70b38b923c7f58640f4759bd6a38e57a351c`  
		Last Modified: Thu, 01 Apr 2021 13:20:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df82bda0265e738eaabcb0367f8de78e90b4dff4ab849162a3a600a3b4b828`  
		Last Modified: Thu, 01 Apr 2021 13:20:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3e1042215ed49358357c1951c9909d6fe8aabc3769b9442d75469aad58b05`  
		Last Modified: Thu, 01 Apr 2021 13:21:43 GMT  
		Size: 6.5 MB (6475791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

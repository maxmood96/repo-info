## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:2a036ad78514c560b4fa3c1f3fca02f6398a4410a764cb8ee8f267c3e841869a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6bc5be80ea8d26ee56b2f7685c7bac227b09842134a120b6556868e54227be49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52298844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74190ba91424fda653752b34d7a98b6d25d44cf2db0b4d90b833245957972ad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:10 GMT
ADD file:4c5e0bec5f780d9c6bfbafcb9e6ed641781dd7f7c2853a0c49d6613e9fef9516 in / 
# Thu, 23 Jun 2022 00:22:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:09:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:09:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Jun 2022 04:09:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Jun 2022 04:09:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:09:17 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:8372a04f222be82bf67eb0010a59644b1e52f1246b3da9034edaa98f3d591cae`  
		Last Modified: Thu, 23 Jun 2022 00:29:36 GMT  
		Size: 45.4 MB (45430020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2745b4737390e15b3d937f284d9bff2f449f076382b63ff32c11d164711303c6`  
		Last Modified: Thu, 23 Jun 2022 04:11:15 GMT  
		Size: 6.6 MB (6572794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03a0ecb31f69b26e47370da9b4d17a73a50bd362d79f044f412d1f06a96f192`  
		Last Modified: Thu, 23 Jun 2022 04:11:14 GMT  
		Size: 3.2 KB (3158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b6c522cbe98cc4c39b415664ba436e2281a79108dd5a40c69fe82b3be73603`  
		Last Modified: Thu, 23 Jun 2022 04:11:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898ae373ff25d4314c9063fa8da31f3a8f543031601614f88c57f2b4ff84b64b`  
		Last Modified: Thu, 23 Jun 2022 04:11:14 GMT  
		Size: 292.3 KB (292264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd158d8d59e117c5ca6a8a105973c7a08b6492fc1e97548a3ecf7f3c5195311a`  
		Last Modified: Thu, 23 Jun 2022 04:11:24 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

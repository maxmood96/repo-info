## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:9a85b4eb32413622dd44f121ca238c92a7c4f981ff19f2419bfdf38552f9060b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:05657b887b9b42d5648a8d9d5da35773a30d5baedd43712b670005429102302f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269581985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bc43d520e31b8dfbda7f1fa1068b8dd3d8b78e1561132bf890473073963cd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad995427cdea099cfee6bb165741e1e35b437f97959525b6b939b6a4ae4df5`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 145.2 MB (145166530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484cdc9d892f8d24a0a112b3f3569947d3b7803f1b3e66cc33cea421f61a9bd2`  
		Last Modified: Sat, 19 Oct 2024 02:59:06 GMT  
		Size: 69.3 MB (69333807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4435e92a03f4e31ddc6cbaf92618cf4b5a82e5b7894af69906cbfcd2e0e232ff`  
		Last Modified: Sat, 19 Oct 2024 02:59:05 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b22b756231f21a20b9f4fbc010d62e2afa44716d20582265f8e1477dab8a2bb`  
		Last Modified: Sat, 19 Oct 2024 02:59:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4392021b59e3446e110f31f7c2001b99a6669682ec6ecc7707ec38244e3b2088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10db8f2a3858be0fdcd03bccd84b72ff6e293ba21e659b22002db824ad9e2cef`

```dockerfile
```

-	Layers:
	-	`sha256:7821037e1a4589f9100d918de7444dcb2bcf9474373998c11737739b531b30dd`  
		Last Modified: Sat, 19 Oct 2024 02:59:05 GMT  
		Size: 7.2 MB (7215198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5215a6930753066bdc4e851261cf1806e7fa3e6e85dc5b57cbb166efb6b92d1f`  
		Last Modified: Sat, 19 Oct 2024 02:59:05 GMT  
		Size: 15.6 KB (15646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55e5437faef092d702e29a932098683a7474c922f17fbebcfa098d1d63285dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267162253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288089bccb07b6f66fca659a29b6b60e7b3593c53ccc5c97a92815b0237786d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da76e01f3707ded82e7b945d61706b260348263f460269d96f132d4d8081f901`  
		Last Modified: Thu, 17 Oct 2024 08:13:51 GMT  
		Size: 144.0 MB (143959463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef05f7e7e527905b09476f4a3fe29502749eecb08b3b9603ce81dfd6f417f23`  
		Last Modified: Thu, 17 Oct 2024 08:17:44 GMT  
		Size: 69.5 MB (69466850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732f5ea9ab2f27a7a144791bca811c23387dc3fe8700e1a3c8d01e677cd91779`  
		Last Modified: Thu, 17 Oct 2024 08:17:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681d187129331cbe66dbe5f563a1317d064310cfb8ccf698d4035eb0a7088084`  
		Last Modified: Thu, 17 Oct 2024 08:17:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e498a5027d97cc4da72330190405d664b0a836e7bef3f4ec58cda429db3f3911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ba7fc780c6cf8c9747d8455de2c6e1cba2d2499c4aea8599d978489921080`

```dockerfile
```

-	Layers:
	-	`sha256:db8e632723edfadb1f0bf59965d542060d075c7f93cbd47b9ea7097ece989145`  
		Last Modified: Thu, 17 Oct 2024 08:17:43 GMT  
		Size: 7.2 MB (7194556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bdf4aa92c39a12743124d8407cd4d6a263c245da7f5073e51a1ec7a1af83c1a`  
		Last Modified: Thu, 17 Oct 2024 08:17:42 GMT  
		Size: 15.6 KB (15584 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f9176d261612cc5a870f2f11fe460a0a81855d573a273afa3c516602a3ca9f82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a9a7d7cbd1189a24af05724a86291bcf3c14a40401c322940460b77b42500acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267162161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d0ebcbe7233dd986b3a1381893d1f165ea225b02672fd5a4b7bb02e42e957a`
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
	-	`sha256:a2cc2b2c001a978151e3adbd8857a7faf4a55640f4e035b9bea7ab040128148f`  
		Last Modified: Sat, 19 Oct 2024 12:02:26 GMT  
		Size: 144.0 MB (143959478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c17022cedcca4f23cf816ba34ca1dacb1bb37783c0f58d092c80d1b801bb9f4`  
		Last Modified: Sat, 19 Oct 2024 12:08:03 GMT  
		Size: 69.5 MB (69466747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d21457a1d2172342f8283652e739f93b4b7137a42f010f62671dd3741819cf`  
		Last Modified: Sat, 19 Oct 2024 12:08:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972c09a2931e6d7904d43e7cb3f623b33d29952d878535375226c6bedc7e4610`  
		Last Modified: Sat, 19 Oct 2024 12:08:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:241dbc3059ff796a27d2ed0fb2d8ea576a413f68e115b0e44d0596c4283feebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e65a128cd19a91d7f7df367563667fc1bce89828dc92b7938955a80064f6af`

```dockerfile
```

-	Layers:
	-	`sha256:a144d64ba4a0b825d7dc02ca4d1f090ec9e8235dc87359a0c4ac6c2f27a1edde`  
		Last Modified: Sat, 19 Oct 2024 12:08:01 GMT  
		Size: 7.2 MB (7220301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ca6bd482d9e1345109ee23bad8c465935669d1b6b4721423571deb38df7929`  
		Last Modified: Sat, 19 Oct 2024 12:08:00 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json

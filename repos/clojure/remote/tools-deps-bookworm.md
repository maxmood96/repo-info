## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d6b7cb349e424c4d0e088c57116c238783042f4d2dfe841b2b5b2fbd8beddfa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ed128ca9451045c45b753217ba4ce436d15a05eefbb94745c3c28cfc462c4c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288085027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d159f19edb8e7afd03a2957584675bfc6a24a7739337ebf76e16623fe4bb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69969815080cda759e4708d7623b3e0ad0d7e53a304d272b025a23e25b04f2c`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 157.6 MB (157568701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503f667df3bc0d0d164115c3b99b250fc311efdf348f06cf9bae7f9a972acc`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 80.9 MB (80939591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ac663ad80a701cd3d7ea6a59302cdb508f7c6a40559d902456b34bfdd17b5c`  
		Last Modified: Tue, 12 Nov 2024 02:24:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdeb19c8b94e8f614b8d61897603b5411a2ccdb9e0c4d1ea51e37473d0467bc`  
		Last Modified: Tue, 12 Nov 2024 02:24:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e42ede4b0219c9482c12a60a181b89999b79f11dc10d52ef9f801373fdd05851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b283f98f32b803aa4a1fd644469175863d996ea05945e3811b98d01c7645e0`

```dockerfile
```

-	Layers:
	-	`sha256:eb207f8288aaab22b57dc00c11e9af7c0dc443c864986781e53a506a502d3ffa`  
		Last Modified: Tue, 12 Nov 2024 02:24:42 GMT  
		Size: 7.2 MB (7187530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a5ffc8242068e67801bcdecb44ee46ea8fc4b22e8e7801855ac28b34c77896`  
		Last Modified: Tue, 12 Nov 2024 02:24:41 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:426e4564d415573aaa8262df77637469a3da029d666f7bce2d7d9917e2cdbfe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286178802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cc05a6b39e9e93507f60d429f5791b217dbb340aae19f4c012c8f9b7fad968`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d23e89cbe4676ccaad92514a135f80ece569c99ea1e9baf773ed88cfce783d`  
		Last Modified: Wed, 13 Nov 2024 00:59:59 GMT  
		Size: 155.8 MB (155793080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f15bdb4a8d4819292bd90fbf170a4ccec98ae636db879e1bcf9d7fe46183b5`  
		Last Modified: Wed, 13 Nov 2024 01:29:31 GMT  
		Size: 80.8 MB (80797482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21d713d1a085e384381a41d5a2994bbd60db0ed979a70e703ec089083830416`  
		Last Modified: Wed, 13 Nov 2024 01:29:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b3ee1ea0f2b814c46326e3d54df2b6bf2248f9bd28c1b21f4a5da26b79be3`  
		Last Modified: Wed, 13 Nov 2024 01:29:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:464cb72061a1a14847ca26057278a93395df03220c4349597c9996f6275a9213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ca0123c1bf52f3296f862234d3654bcfb499be5f7da34c0ea3bdc6efd0400c`

```dockerfile
```

-	Layers:
	-	`sha256:4a8fcbe744b89a228d76e4b911a15d009d41a0bc19cd34a6b3e1de49c4c8a254`  
		Last Modified: Wed, 13 Nov 2024 01:29:30 GMT  
		Size: 7.2 MB (7193370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1028add2fa6b5bcff7d06b56a77ca76d87528801433f789de6700ebb3a92602`  
		Last Modified: Wed, 13 Nov 2024 01:29:29 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

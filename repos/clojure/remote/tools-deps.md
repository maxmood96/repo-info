## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:563480c1dae4aa597143c73c620f35c0c5fd4d37e9a068e9b777559519b5d660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

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

### `clojure:tools-deps` - unknown; unknown

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

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7380e80ecc16e6c0957aa098cec1fd9cff71df841b106e718176767f2242b5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286169156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b9a198d7bf2db8a7fa1b5a3304cc5ecb96f941e3fe2eb506a93489b508d5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ea3eac04a80b5e18d7d58af963d256a6d692ad00e74729e22413155362f24`  
		Last Modified: Thu, 24 Oct 2024 08:50:34 GMT  
		Size: 155.8 MB (155793073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41f83781f4ebbef83ada558d6e1db36f91155af48ee46504889e78114bcabd9`  
		Last Modified: Thu, 24 Oct 2024 09:30:39 GMT  
		Size: 80.8 MB (80790067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567b42411cd2fd64590c44fdf2fe435a23763f857c958e7bd152ce1af650348c`  
		Last Modified: Thu, 24 Oct 2024 09:30:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3b124dbfc9e4277713bd904cf009ee8e47abc8520bcffa21635225f655db39`  
		Last Modified: Thu, 24 Oct 2024 09:30:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:18d283e6cde338372efb214988036779f212254cf50306f57aec44dfb1048475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cfdadffbcccfa57b4ddaccdc97160bb3f806146f49be91ee4d7cf7b34e2e73`

```dockerfile
```

-	Layers:
	-	`sha256:9a0e70f0fee8432b67808d5bdca7cb9674aec7c5dfe678d927cbe4672565fc04`  
		Last Modified: Thu, 24 Oct 2024 09:30:38 GMT  
		Size: 7.2 MB (7193334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74ef3b024266ff5dd31185a133cadd6842cc35786152b2e677bfeb1747abc9`  
		Last Modified: Thu, 24 Oct 2024 09:30:37 GMT  
		Size: 17.8 KB (17830 bytes)  
		MIME: application/vnd.in-toto+json

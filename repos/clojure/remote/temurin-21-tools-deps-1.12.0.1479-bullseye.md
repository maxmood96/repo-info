## `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:49a9e12d90d478bead2fd7331fa4b61727074b6a6c369bd7c5caee3c7cadcaf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ece1dbd97517279ac020467b8903ab4ee00cbd8933f561dbfc16401d0617ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281817874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b2f9e2c69074a6dbb9e04c309e89cafc8254eda3c6e11fa84ccca5209ea2fa`
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d456ecc711ecd6f4598460dd07513722ca01ae080103586d3f4b078e92a9ad64`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 157.6 MB (157568675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9676fab119eb8c52526ea56f2b178a3b72d1ae9989b7fbd0f6288e5cc5a2ec66`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 69.1 MB (69139378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656d7b10d0a4c8506c1d638b07229a18bb8dd96afd010019d8103eea117181a8`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580e016e303dcd7747db911f744f715bf790192e26fa8e50dc1a1581b503d5a9`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9d6e328c9e23706e32706781009cd249692937103645c5b6fa9699fb945da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0850d67086270ff7fc05220fc4ad13dbaab91f0a24496edb0d703bc4149b42`

```dockerfile
```

-	Layers:
	-	`sha256:29d8afa24c2befd32402ae8e8e0a216ff12be3b8fe4a9c5f22986e2884e8e8be`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 7.2 MB (7219653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b91ba314c34451bf41e0a857a1cf7ad6893a37da5102d186f9f0705379f2a5`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a29fc9b6d3c56e779802dcf4421bc32f88ac47827507ee909a9029c0d48956ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278827455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be636bc23da1da77e61b152c5e9149d33d1e208f1d82b75a1412d8513f32547e`
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe2fc906056795db59cbbec672365f3ce425ed8a02c6b0a2bf0d4e922caf66c`  
		Last Modified: Sat, 16 Nov 2024 05:39:29 GMT  
		Size: 155.8 MB (155793109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f863c5a54ada89eb751061bae338acceb5ac8a32cea67826daf623c05d79eea`  
		Last Modified: Sat, 16 Nov 2024 05:43:56 GMT  
		Size: 69.3 MB (69276232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d38eb27871864bb3c00089fcec256bbb0dd42c8d374c6695a02ee040ee9ef`  
		Last Modified: Sat, 16 Nov 2024 05:43:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c267ae9a40f45e04bd77bc541420693cd1b616adea22af1defa7cc8f4e8c6`  
		Last Modified: Sat, 16 Nov 2024 05:43:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b342ca4e6755645ed8d9e1de95310b107b20e0f343cae34669b4b606b14ee681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38e4de4ae89287d0d454bba52ed38d324cde0629c7fab75287ecd5f709a8ee8`

```dockerfile
```

-	Layers:
	-	`sha256:38361d3a1d97eb33e9da5c720a7390f6d13d4d1c4cc9257c35688ac29142b64b`  
		Last Modified: Sat, 16 Nov 2024 05:43:54 GMT  
		Size: 7.2 MB (7224780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cd780d3c71183df9a60f760fb81f52997d14343c1eb8e42224387f414571f0`  
		Last Modified: Sat, 16 Nov 2024 05:43:53 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

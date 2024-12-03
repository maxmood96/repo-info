## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6ac54ef287dfd93f2c8369d6b01fb77d8509eeb7c94bd7fca45776bf055064e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:613fc7f582329abf808d6c399a5c6d429021dafc2572056778ba536005086b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288194639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06579794b01625e7c4aace3f25a228aefc82a42747218dcd1011c71d51c9ab55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918f1eb549dfc6bdb6ccf7e5abeb0cfb05d68cf9ff5341d3f75274a6a3dcf9a`  
		Last Modified: Tue, 03 Dec 2024 03:26:12 GMT  
		Size: 165.3 MB (165295086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8420d0d862917e0b562f9dfc5c99f50e1566c14d4453ece1f1261c0b346461`  
		Last Modified: Tue, 03 Dec 2024 03:26:11 GMT  
		Size: 69.2 MB (69159369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44675d7fafd219c837cb476b73a1cc565fde7f2d71eacd64ffd4abe8da478af4`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fb45f6b3617cec2b98db343a5d070cb93b57f3cc6422c8b4ac8a429de3ecaf`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:17b32d6547458496a57e8494a4ebd718cf9ad0cc38d3fb992597ab40dd3e3532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c54e4c9a7a4d088acff1a29960b771b8cf87f1904a47998f560291264ea85`

```dockerfile
```

-	Layers:
	-	`sha256:8ab38f1c11f3139ef5745d41a52dee958c1bca438a66906d26ce2b71992a41da`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 7.2 MB (7219080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6e4794132e5fe9bdb8c7ad0900fe50b6701c92fcac055dce5058aec987bea1`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a45f73f09977c827d3ff05f2c3c5c68e63be1f7376bb1c254c6b553f76b7d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286316088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c1e8748489d348c3ac241dcf34f1f9109137f9a7038768dea28e0790e05039`
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
	-	`sha256:491e237a3a64d9dd56b1f0a09db804c1f44853b80f60022932440da3535ab14a`  
		Last Modified: Sat, 16 Nov 2024 05:48:45 GMT  
		Size: 163.3 MB (163281799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac9e2d1b63eed6cdd68ce451742c26b67a46b768dc2718170b546f1fc48bd08`  
		Last Modified: Sat, 16 Nov 2024 05:53:21 GMT  
		Size: 69.3 MB (69276180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853802622c86475092a26299f86a3cb35effcbe6ab2d9046571293a4e5a6a7dd`  
		Last Modified: Sat, 16 Nov 2024 05:53:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842ff0f0702b8c29f855b0d64aa0a2756d4e5f184815cfb2332cac73093ce6e9`  
		Last Modified: Sat, 16 Nov 2024 05:53:18 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:45d846c7fd520d83f05408d7e737c146b7b5f0f8d7d8114ba910d6e106b9ceec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e468c0f91626b2d3d90bc85b5ba7a5cd84098152d39bcfeb5b9ceacb23056`

```dockerfile
```

-	Layers:
	-	`sha256:3982e4877d47671da5b260e8b9d5edaf59a49aa5c48cb9b91080951d159d6c5d`  
		Last Modified: Sat, 16 Nov 2024 05:53:19 GMT  
		Size: 7.2 MB (7225364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de856f207c4dbf734c37a343d02fd7b0e53b4b263bbe7296b64c48607ca84d05`  
		Last Modified: Sat, 16 Nov 2024 05:53:18 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json

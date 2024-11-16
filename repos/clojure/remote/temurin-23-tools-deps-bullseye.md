## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c21e56d551ab97288fc78f59063c35d0a3f434fce57df965a6f6fa9d71207870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:117eee6c4a26e01f8eb9c1bc997c3a5935f834e37afbe137def42157fffab51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289544104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752afd3fa76e9fd0de2dc9f6f964ef579e1db7f3f4c69cbd18f51251f4b066cc`
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
	-	`sha256:2a01a4b471910478b170aab963449623d4ef54efe329970c9e48d9bcf2f5afa4`  
		Last Modified: Sat, 16 Nov 2024 03:51:47 GMT  
		Size: 165.3 MB (165295136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434201c854f356eb31ca3f49c9e62247519fad5a258921a309b8afbbc4ed7a22`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 69.1 MB (69139150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a39dd3b24f1f96be5de1ddc08f8388da0bf33c63cc077b071722393f2d6fa1`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706bb694f7ee5b7eb3e825bab9a54c5731b4d35e24a232c868f57cd64e12a7e9`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:06d5c2f4f5f453e9acfeea6539d1e2a21289f9d7136cf8802f317035b10ee957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bbd021a49a5641e78c58fb17c8bcadc4676d85d02f6e26d3bf8880ac6a56f`

```dockerfile
```

-	Layers:
	-	`sha256:8a01ccab342b13cc9d079c17163d26f8a5e8e112117a03ddc0979ded197ca1e3`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 7.2 MB (7220883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00ff6e374242a7da3a0e8b22f3dc098d7cdbcc2837e2ab49c3a221a895dcacf1`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 15.8 KB (15819 bytes)  
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

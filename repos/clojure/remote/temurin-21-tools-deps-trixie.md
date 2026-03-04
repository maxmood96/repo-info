## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4b1e5759fcfa20e421f4a818c64b98e12abc82a061e29b8b9e74d7b7d73b184c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c1bd2f905e390afdd3fbe02f32679fd1e2ea81bb7fdd80da11709dce161b7c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292718217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cf6789f0d567e7ad0734a1ea555ce12412f9b42dfedfa3fb6d62310a439f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:05 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:05 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4aead82d53ce2da7cb9a67acf48d5dcabe8e5ad251beece3c6c53338fcb8b4`  
		Last Modified: Wed, 04 Mar 2026 17:51:49 GMT  
		Size: 157.9 MB (157857067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88626aea0e1adec7604427cab9a03774d9b9a1ee5630ec3ee81a2c3566357852`  
		Last Modified: Wed, 04 Mar 2026 17:51:47 GMT  
		Size: 85.6 MB (85566988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6fde22ede0a5c4c59abc4ee514e2fc4d2900b0ee7341ed49d2e966b0f93f28`  
		Last Modified: Wed, 04 Mar 2026 17:51:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6a826d6ede754140eb4d3c5e42c1cd11e080283c08392c3fc9e0184e1069a2`  
		Last Modified: Wed, 04 Mar 2026 17:51:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:669c0c37e88c5b798fd78134429274b278aac27bf63433bad32ea339cbe7f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774eb570774abe6428bf5bb6495d3d1053459df62080fe5165c6dc918f2e5ed1`

```dockerfile
```

-	Layers:
	-	`sha256:29f88e8614a1c2cb2902e161d52c0f43178d3634aaa19dc8343ec5fedafb5f7f`  
		Last Modified: Wed, 04 Mar 2026 17:51:44 GMT  
		Size: 7.5 MB (7472445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caee4108643c384b09f29efb8c9a7189c78210978a049bd0dc3633753095cfc4`  
		Last Modified: Wed, 04 Mar 2026 17:51:43 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d090d8939421620f7d7d02cf73b3cd2481d76dffc8e4453fd7c6d6aca2f9c23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291169044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f559128b320a8344ec64f51f0f3a885736b25000eb7cd9079fc6d661ed59f86f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:38 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:38 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bff89f68d7b43582d381b8485667924cfeb11ea4f48b49e2aca0a328e59adca`  
		Last Modified: Wed, 04 Mar 2026 17:51:18 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ee176d90a2e89978395d5d0f5378ce3288b0864aedb23f3049586f47d7768c`  
		Last Modified: Wed, 04 Mar 2026 17:51:20 GMT  
		Size: 85.4 MB (85382742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2550c8b5cb9df0ed9f6745e15229812fad5255f1914515752ba43f134be69b`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efc04d6bf48db456356f359bb5df46dc09fed6367a17d31478e5f9f58dbd06c`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5b78ea0748613ace5f8976d4cb7e7e2041b295d8bd9dfb7dc9582003c8b20217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fac66e607c887e9a750963817a5361b432c8efa068fc9433579b1b5a4378584`

```dockerfile
```

-	Layers:
	-	`sha256:d720b91375ddd7ffd382700d7aae30e02650a117811e992e22d3a6940d54bfd5`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 7.5 MB (7479475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d17360e5f930d9f77b455bd79d4eab3f1673a103d02b087bc9af2a904bb72df5`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:002251daa440d22ec76f4a5a304eec0ecbae88777af9634810814d1219b0a1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302067082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa141626460ab2765c2ff9b40d9ba566bf15b3ca72a51d3c6d88d6dbcdbbc3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 18:06:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:06:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:06:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:06:35 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:06:37 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:07:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:07:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:07:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:07:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:07:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc943037c08348e6dd23042b1f1f5e0d80087e8f7a2258ae7d75d540fa8baad`  
		Last Modified: Wed, 04 Mar 2026 18:08:19 GMT  
		Size: 158.0 MB (157977516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944dd5107908887bfe850a197041824f382754bebaa60437c205e284996771e3`  
		Last Modified: Wed, 04 Mar 2026 18:08:18 GMT  
		Size: 91.0 MB (90976259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebed8ecf4b789ac83ed962f131cc580c0c115b9c74773b8af60bcbebb9e7ebfd`  
		Last Modified: Wed, 04 Mar 2026 18:08:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a73ed9a6a7a810acd2fdf0d3a3fcdc6532e0b29b4a6bdc92bb0146da3b4b77b`  
		Last Modified: Wed, 04 Mar 2026 18:08:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2e415da48c43f18c6bc88e4cf8e75f5f3750498ea73a267c22eb805f9722f41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfdba8905d016cee69494f5f44bea0ef727f1625590cd1957c6560ec895ded8`

```dockerfile
```

-	Layers:
	-	`sha256:744fa75f7919c5fd82f6d43992b5db61d9d89e238d43d58e572be98ea58d8e9c`  
		Last Modified: Wed, 04 Mar 2026 18:08:14 GMT  
		Size: 7.5 MB (7476866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a251d79ca7d95250adbed003d64f95ab3b6b419b13fb97576a95353cfebd4e63`  
		Last Modified: Wed, 04 Mar 2026 18:08:14 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d0052c664fbf97f07169285e77fe21a9530c75c9af44b5e3ffd9597062a12143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289434722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb58029fefb2c062eb59ed1033a854a4c6d947146fb3ccbd939f0913e49f58a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:14:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:14:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:14:59 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Wed, 04 Mar 2026 11:14:59 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 11:17:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 11:17:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 11:17:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 11:17:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 11:17:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb9c79161005e6b84d0763b0f118c07cedf15f1b6ee06d958a2a83ad03907d3`  
		Last Modified: Wed, 04 Mar 2026 11:23:14 GMT  
		Size: 157.2 MB (157216889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7307b3b20b3a55db8c7968b6249873f1aca5efd60334695ed2038110c7b3e27`  
		Last Modified: Wed, 04 Mar 2026 11:23:03 GMT  
		Size: 84.4 MB (84439852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d4ab3872fc67dbe43a18163a381cf3091428c74ecfa20bd2da64a8675a38b`  
		Last Modified: Wed, 04 Mar 2026 11:22:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458576d305a181e20e622df93b231769264166d82bf3d3f6c824a81c14299e03`  
		Last Modified: Wed, 04 Mar 2026 11:22:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f9956efd0c40a16f65d6c9790e9c9c908f2d5093b3b04ff525c14f4d2670720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941da767d2e3b6ff8a6b4ea4a54bdc41de7d2e706364bcc902c3ea05913a045b`

```dockerfile
```

-	Layers:
	-	`sha256:17338121e0697a258f04a7ecd17e33f1f8541c148f3e7794584d5fc6a79a5e12`  
		Last Modified: Wed, 04 Mar 2026 11:22:41 GMT  
		Size: 7.5 MB (7460360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a00d93dde3e1e5d1368c625c2c17854850c68409e1e3720890ffa093f60e604`  
		Last Modified: Wed, 04 Mar 2026 11:22:38 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4e2f768650189ff3c3f360787037560f3c7e951de0636ed6a9fe73d4bdf2e34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282990447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c093ed7d0fa51cdd61ac74251ba561d7f574e021f91967c117ca7dc42367a08a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:20 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:21 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5fd13380d1d6dd029ada7308991e8576972d2191c946e30cff3386b69b1cad`  
		Last Modified: Wed, 04 Mar 2026 17:52:10 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f86388044865d8bd5ad85fa5f447b41814299137d59bac575bd16c1a38a4793`  
		Last Modified: Wed, 04 Mar 2026 17:52:09 GMT  
		Size: 86.5 MB (86529570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb9b62688fc11c0b29e0911b33df0409931d4b4b0e03914f560a7539d15af8`  
		Last Modified: Wed, 04 Mar 2026 17:52:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925b5ac6718cc3257625d860d39715c3ad4d3593c3d508a21ddbab7a7ea8e89`  
		Last Modified: Wed, 04 Mar 2026 17:52:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d84838248a8325c10119737c54ab8ef87897c52846842f46dda7261f80aac4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147eca1fc98dba91b2ff83d60918b78aeef70f9b60bab6cd31a56926c13d8b1b`

```dockerfile
```

-	Layers:
	-	`sha256:1f06cfee9511980335bd43462cd482ec9afa5c255dd1ccf7331563e26eab9de7`  
		Last Modified: Wed, 04 Mar 2026 17:52:07 GMT  
		Size: 7.5 MB (7468367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dee877f83b1b8033e56f61e5d9c80d7ac6da7a6449a02af3fb78170da1ea858`  
		Last Modified: Wed, 04 Mar 2026 17:52:06 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

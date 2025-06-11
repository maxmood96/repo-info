## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:6b6e219d4be854b7754de601507b9f1b41e21064e4c25a744bf95ed320d05c86
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

### `clojure:temurin-24-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:370c7a32d596afb0863cb44175ae322415ed35ac1de890cda56adfac50dd0da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224472147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8075dc8919c4d298f6037c7983ea893a49b8bb43f2aa2064f8fbe8c95f7222d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2adaf2d302dff995b392b04413c7bcfc1bfc259361a125e6097861e134878d`  
		Last Modified: Tue, 10 Jun 2025 23:53:35 GMT  
		Size: 90.0 MB (89952004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f067096f768c574b67857d3a6f1eba6a371bbfcfdf33a79a8afddc106ad1c`  
		Last Modified: Tue, 10 Jun 2025 23:53:33 GMT  
		Size: 85.3 MB (85265240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a21365f8d36a5a109015fa5a2876aeeead9fa6f8d82da9e8853e48c8332150e`  
		Last Modified: Tue, 10 Jun 2025 23:53:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83e6f507c14669bc5eb2c1191dc7479823a460a63f90f08dd8f08e918f3818c`  
		Last Modified: Tue, 10 Jun 2025 23:53:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:49c2b8c3016986477ef1e5d1379c1d436c6298c5a03d3a0cc10c4fc5d2e5313a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2469ef02080a152e5d44db92969f4bb92b841ed5e99672b4f4f4ffb92b83f7ba`

```dockerfile
```

-	Layers:
	-	`sha256:0cd48d37ba7d81ac3e7793ba964a0210c9ddb65ba98024df124a0b91656c4572`  
		Last Modified: Wed, 11 Jun 2025 03:40:58 GMT  
		Size: 7.4 MB (7409795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f937143c5e422c52ee3e39266fd5f092191bfdd5b0c3fe5790cd97686db79a`  
		Last Modified: Wed, 11 Jun 2025 03:40:59 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c166f35c310e5f13c30cde8feb932a82ba4353339328628ff37a70fe49f19f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223910213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c546fab7770b1562de93fdd05e040579f03046d5a65c08504f597995f4a2140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6727a70b0f439627ca67f9c6ba9724699951021773f09f699ed385ccc265116`  
		Last Modified: Wed, 11 Jun 2025 08:46:03 GMT  
		Size: 89.1 MB (89091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3f71271a7578377b8790a99f302805b4b3da5e12bb3c7069fb6636ddd419e2`  
		Last Modified: Wed, 11 Jun 2025 08:49:53 GMT  
		Size: 85.2 MB (85196366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6e40f00d201f2c3f3376abdde5570b66d6ed5cb73c7224c38049544b269c31`  
		Last Modified: Wed, 11 Jun 2025 08:49:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8feccaa0ba0b2392882a48f966f987a5d68feb308ee0a494d80653474bae5c45`  
		Last Modified: Wed, 11 Jun 2025 08:49:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8e71558c5ef1b4c5118d7242c868d5ede790d2bb89b16eb747aaa5e4979cde58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c52701f7321a92bb987943b6f2b9a317c919897f004633ed52ba4c5f03fc12`

```dockerfile
```

-	Layers:
	-	`sha256:359f34f47906f0ca1721dddde0864098ba0b48a58fc6e182d8936835a4591691`  
		Last Modified: Wed, 11 Jun 2025 09:42:12 GMT  
		Size: 7.4 MB (7416822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba25b0ae4b042269a49fa2ef214d59a4eb6c2bcb268c33be489a456556c5058`  
		Last Modified: Wed, 11 Jun 2025 09:42:13 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:79fd4d69e39be137ba19ee14912ddfaf3d2392a81430f0fce8951ab57d2b2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233784489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dd47bfa2646e8473aada8396701af51ca40341c29919f15321da6f4dba36bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ca9600ce19941bd1ef3c8d0e4efa1b226a4a6ca057fb715495ff8c8a57501b`  
		Last Modified: Wed, 11 Jun 2025 08:55:40 GMT  
		Size: 89.9 MB (89920261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b242f0dd40afa8d781e9b563a0af8e2ecbc64f626f3fa7449c12a7e2e60e1a48`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 90.8 MB (90772251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451882f2c1c239e661e02b0567f46524de8cc60e99402269bbd7382d2b8b1578`  
		Last Modified: Wed, 11 Jun 2025 09:02:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e36daf64a389b94f2e9faa584754be26f60e256fc534b4c2ea1fe138d03afb`  
		Last Modified: Wed, 11 Jun 2025 09:02:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:636f26989dc42bb8bde6b0b88ad1cf116b2f021d26e2fe0372470f3ece7b32d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a45c5943db786e52547a346513dcbcfd0d721f5dc6eb796d5428d70bf0e9e6`

```dockerfile
```

-	Layers:
	-	`sha256:bf7e8e46a4f9e5c5fa74670c39788d3a6272ab92af92e39e25a2ff3b747f3c6c`  
		Last Modified: Wed, 11 Jun 2025 09:42:19 GMT  
		Size: 7.4 MB (7415510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18ce00c16d3ba400876eaa8f966feb080705c3c28e10a5d50d0fbbd1d65c22c`  
		Last Modified: Wed, 11 Jun 2025 09:42:20 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:97ccd42bf8034692c10fc1686dae9ac2e3a05a482d4478a656a97590f463d108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219608859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66240f11a36161c6d13391a69520e05e323db442af3e24b24c989b710ded4722`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9b364e93ce76c0a2d3ef70f055ab6d291b7cb89ab88f97e1fa7b55d06fc05d`  
		Last Modified: Wed, 11 Jun 2025 00:54:24 GMT  
		Size: 87.6 MB (87622237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7fa0fceae23a794371386998579abf2ebb78f84f3f34969432aa55b5633153`  
		Last Modified: Wed, 11 Jun 2025 01:28:23 GMT  
		Size: 84.2 MB (84242232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9704b369d192dfa30dd25ef7554cc2826af5fe2f819afc5014537f3259b23144`  
		Last Modified: Wed, 11 Jun 2025 01:28:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5b1c2175c5f368239deb1c572e24340ac39f099a50b63c9ca77cc6289fc16`  
		Last Modified: Wed, 11 Jun 2025 01:28:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a2010940f955e7369ac2c648016ced17e4bbc2f58958fc352054d33dbaedd0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e084a40ca31d5fa591e42548e7cc5ae518f96e81534fed7cccfa13a7526aa0`

```dockerfile
```

-	Layers:
	-	`sha256:98a0ab923a8a201a285df3ba78e9792acac4b95ab25e43285be7425c104d2a00`  
		Last Modified: Wed, 11 Jun 2025 03:41:15 GMT  
		Size: 7.4 MB (7397703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6074bd64ce9eb75e8db08d17d514bf8c3145200510c9c1e311de09cd671c7348`  
		Last Modified: Wed, 11 Jun 2025 03:41:16 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:490e962820fdfbbf6fed6851f2b967a48cbbd4391782c65769f01521ae711f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220895352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a099b6a12ba90325f059807d42745179765414e43c346683cfd8a4948c09c3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324df67e9f501c6e7bd756b604eeb1328e94a61583e56a9b2200a3d1688fa5c3`  
		Last Modified: Wed, 11 Jun 2025 06:00:41 GMT  
		Size: 85.2 MB (85216806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31d010e4c11b4a75ea410f430ef8bfc43b6efa440aa00c33297415b19042a1`  
		Last Modified: Wed, 11 Jun 2025 06:04:01 GMT  
		Size: 86.3 MB (86347738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b8258c787215dfeef2fedb582460fffcee6456f50e5123c651051f09c26d20`  
		Last Modified: Wed, 11 Jun 2025 06:08:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89902d30d828fe2df5c3a7a6ddf5e113fdd5e1a0b48bf0ba5a1ad9c0439f6c16`  
		Last Modified: Wed, 11 Jun 2025 06:08:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62b7457f055a44804260a28ee8ea9e78178763e10e6710f1c0ab9227456e3a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e331af7bac0a2ae40211d159dcbc21d4002bf3021423b62fa98081db5b20c43`

```dockerfile
```

-	Layers:
	-	`sha256:b9ef18737bd992781afde4eaa7aea086a8e12cd7c48f479563f251f5d0c2948a`  
		Last Modified: Wed, 11 Jun 2025 06:39:51 GMT  
		Size: 7.4 MB (7408265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf31433416c543e60dc0a94b79d92d993579a29399d3ed70bb06afb6626c638`  
		Last Modified: Wed, 11 Jun 2025 06:39:52 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

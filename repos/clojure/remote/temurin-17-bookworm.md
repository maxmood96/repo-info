## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:c79e6c0e0d310deb417dd538503e58a89736d4879d8771dfe4e1272683d28dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:63205b7f0bb8ef497437bb3aa6a6aa2a8a16bbb204f0bf4cf7139c84ef20890a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274117885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7b9782f22e92c1f59d2bc8629b5f7acd5b1d3d6c557d45a65fbb29396a2d5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec0f1956e0bb036228054c2dee06347828e7043c017da027a6c7706306de00`  
		Last Modified: Mon, 09 Jun 2025 19:42:34 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82f8cd4adc2106763fbe3d1d0bbc7c3a62f8eb7a756dbee5314282bee5fa16`  
		Last Modified: Mon, 09 Jun 2025 17:19:06 GMT  
		Size: 81.0 MB (80993636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af762ea5b6a93166d49a2da612faf920bae6f3346773079c628c1cbd38b9756f`  
		Last Modified: Mon, 09 Jun 2025 17:18:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21a3c8477896b4567ff9d24a9091ad2fe7947d1fa27d95c6803c7504e55b09`  
		Last Modified: Mon, 09 Jun 2025 17:18:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:60ad58c7150aebb3acfce0da39f5e6c4cc2caf218c704035f3a383fc2998f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b3147c8cd67062e2f5747f0c60638c6b415463ef5871be9c1e2f326f55b1b`

```dockerfile
```

-	Layers:
	-	`sha256:8837f75b084e08ee0918a84406b1a8360320c77ac0e03d354c62a219ce5d42e3`  
		Last Modified: Mon, 09 Jun 2025 18:36:56 GMT  
		Size: 7.4 MB (7366912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb438db498b2455677d0a05476916cb973d41262a2573dacf769cc356eaaaa9`  
		Last Modified: Mon, 09 Jun 2025 18:36:56 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f9acbcb30595447404feb62cc08624be167ff25d2d9973c64944118781d64f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272689746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bc76749e5f56aaa35f90b13502400c03b5ca9cfdc0706f183a9f67de358866`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d616bd6f18b21e8af2a1fae7e0a03786fe00872c2eb14456c4dc4039bfa80bd4`  
		Last Modified: Tue, 03 Jun 2025 21:49:58 GMT  
		Size: 143.5 MB (143512624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e983003ee99b66b9a932c65c15dbb32a1607197c438303a96a0d4d33c92446`  
		Last Modified: Mon, 09 Jun 2025 17:45:41 GMT  
		Size: 80.8 MB (80848898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446bba9216c6ba2a354abe409d08d5a7bdb014264b5dd0b67e98124d9c8150c`  
		Last Modified: Mon, 09 Jun 2025 17:45:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a30b8e3eb5e8f181dc17382489927c9607523d8264376bac4f9c0c9632de18d`  
		Last Modified: Mon, 09 Jun 2025 17:45:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4ad4f9e406dafe57afdca8596e47b15540b7230929a7d923481a4751e25e1b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126db867b4e1a9d025089d0134b2e8354ec47d583accd931c9bae82b9b00a0b0`

```dockerfile
```

-	Layers:
	-	`sha256:4bae086015aa9791b5798804fb06f5c8dd5a3410aefe91d45b774aa81e934964`  
		Last Modified: Mon, 09 Jun 2025 18:37:02 GMT  
		Size: 7.4 MB (7372675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b864199416bd7e4c1583b9abf756df3561e5b45bdc00a12270f1fdc005b4a3a`  
		Last Modified: Mon, 09 Jun 2025 18:37:03 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1ddb395b372b5ecf3deccaa4fd5c2621808eb975ff40e5c06401c9a309f6fee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283426441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e11804c6fe93af4f972792c7e326c7f21845d05bc41902667fc8abf4b1e123c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5fca0800952ffd845ecae7a757898651fb9b497615be2e0d7662f4d7ff229e`  
		Last Modified: Mon, 09 Jun 2025 19:43:33 GMT  
		Size: 144.3 MB (144280554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fdea58503233f896127597d21f161ec301bc856ce033344292ddcd6bd38502`  
		Last Modified: Mon, 09 Jun 2025 18:00:37 GMT  
		Size: 86.8 MB (86813226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bea87ee18ff1be50f0396c76d67fa9c1eba512c6032f32c6e520d6765fdaada`  
		Last Modified: Mon, 09 Jun 2025 18:00:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8b3ed57cc76283b5b87d609764bf401310c7c4a695ccb82892a893e9431864`  
		Last Modified: Mon, 09 Jun 2025 18:00:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50fbe7b58b4b86a28e121510789cbc1ee3712e049e4a29f0d6fc4871d0e8d066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14d20e2d316effca5768ab922b1d435938deb78bca90c97c3c1e07a3f90866`

```dockerfile
```

-	Layers:
	-	`sha256:6754db586b259742bec60940edbadbadac8487eac54092b2d62fa67000b3609c`  
		Last Modified: Mon, 09 Jun 2025 18:37:09 GMT  
		Size: 7.4 MB (7372116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa7b311840839cf04c14a4b62b6c23406a94459f9de533d283234e2219bce9a`  
		Last Modified: Mon, 09 Jun 2025 18:37:10 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:daaaee7c8ca4edecb9e65b9af3aec1af26567938f1a1de4fe2f88363596566f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261621297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1573810f72bbd768da92fddb7ab33922d71970e6462706c7ccba74c35bd4fc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f22e4165e784cf5cf4630de4aad9261205dcd457d5c03fd507e8f308626656`  
		Last Modified: Tue, 03 Jun 2025 06:12:24 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9216e9576ba9f96fba2ce3bb82a47ddf44c56adaef0398d0209fa32187f7a`  
		Last Modified: Tue, 03 Jun 2025 18:31:40 GMT  
		Size: 79.8 MB (79802867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd521c64c3c3def1c528a745008c4f312a396051f7dfe93fe6700cc339fa823`  
		Last Modified: Tue, 03 Jun 2025 18:31:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c5806a8c2dfb137ac8b6d772b1f0a3a5131fc59b570c335d0bc68da4dd456`  
		Last Modified: Tue, 03 Jun 2025 18:31:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d712268a34f5c255d93015836990c07934d0f08d2555bec1394cd9c2de51e764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb556484a8ab0a9d63ed16178908082d64acb501d456016ad208dbfdd18ca5b`

```dockerfile
```

-	Layers:
	-	`sha256:4f4df6a2912f0c0ce2f7ff74f363292bd1354d93b712ed2fb53df62f78d65c1b`  
		Last Modified: Tue, 03 Jun 2025 21:37:40 GMT  
		Size: 7.2 MB (7212733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbcf78c931e8d52cccacbdeb46a22f5136564059d2318a962df58da2f17e493`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

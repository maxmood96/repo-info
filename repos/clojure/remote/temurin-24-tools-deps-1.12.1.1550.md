## `clojure:temurin-24-tools-deps-1.12.1.1550`

```console
$ docker pull clojure@sha256:b5dce5863ea63011509fd25fed31126fef5ccd1f7300716ddfa8ae5993e65812
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

### `clojure:temurin-24-tools-deps-1.12.1.1550` - linux; amd64

```console
$ docker pull clojure@sha256:d196f6b751eb380d13d821c2798e818149c7cbf60068469b72534a3f5d02172f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219464567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942a6b16048b89383b95ac950ae4a071cf636af82e7f381955a96284155b2318`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccff9f67db86aa90c6aca5f4e6dc5ba764d9922b59e5b565c2143512d1cfbf33`  
		Last Modified: Thu, 14 Aug 2025 04:20:21 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f843a18791fb9a3593653a12c451747a50d0036e435315df18919ba7cdf2bc82`  
		Last Modified: Thu, 14 Aug 2025 04:20:25 GMT  
		Size: 81.0 MB (80993790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f607e2c1672f3c2d50264673e8ecf93367742dd2c950d7c39d1991eef903b4bf`  
		Last Modified: Tue, 12 Aug 2025 21:44:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8165b6eed5e1347e055049f99b2909f8719e13f03290848f31c78cbcc4c7b2`  
		Last Modified: Tue, 12 Aug 2025 21:44:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:64048dd4a5b3dafb5331ecaf72ad31a57e11569fc41cd7ed897bb43c69021e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab88c268c2789499b1bec08eac88e2adef254c3f50f84dcda48df05098e76db2`

```dockerfile
```

-	Layers:
	-	`sha256:9c73ab55160c09028b9b50c6c596ce5216ace1780cc96656d1f51386ec8c28eb`  
		Last Modified: Wed, 13 Aug 2025 00:39:47 GMT  
		Size: 7.3 MB (7319600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa89d3c51e5068c7c76a0870b592f3993914a5ed453fdd551e1aca15fab816db`  
		Last Modified: Wed, 13 Aug 2025 00:39:48 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eaa8cf20bd9ae945e852b5077622f988054cfd2d2f5c3ab894d59821d184fe3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218304331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deaac55656eb57496cafb914310513485c4f57b0fa9aafc9c94c731fbbef43c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04332eebace5c1a58284af96e3173cbbc4da8a720d67bec11726cba4ec418852`  
		Last Modified: Thu, 14 Aug 2025 09:01:10 GMT  
		Size: 89.1 MB (89092517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a85d4b6058f17e8a7ec2fbaf0712a3e598da5087fd2031ed676bd612faabf`  
		Last Modified: Wed, 13 Aug 2025 14:47:01 GMT  
		Size: 80.9 MB (80868323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0906717eb2cdc39b54cdb6d35e20011a9150a533202ed7fa04d6863736b5366`  
		Last Modified: Wed, 13 Aug 2025 14:46:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797460ccff9caaee5bd18682d521aa3ccccdc8ffb265718d71cbc5eb19c9d4e`  
		Last Modified: Wed, 13 Aug 2025 14:46:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:5c11f6c0e1cc3b3fac4059a55759d9e15f077590a9d1825f65689489924bae27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe06ae4e6f12dddbdbc366b9c9717e1506fe9ac47421eb1f62d7acdc1925408`

```dockerfile
```

-	Layers:
	-	`sha256:d6bafb5373cc8f9a51b6a8521f444f76e07fa1943531ff871919b04c46a99526`  
		Last Modified: Wed, 13 Aug 2025 15:40:17 GMT  
		Size: 7.3 MB (7325384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667b40fbacd085e72471aa09f013d18e53a0d2f129ded29dcac3bddda995da96`  
		Last Modified: Wed, 13 Aug 2025 15:40:18 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550` - linux; ppc64le

```console
$ docker pull clojure@sha256:9da587d0f4023155d80266c569a87817d833a2c7e2edc995ce079fde9431c34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229079452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e368567abe4373220276352ac06b005f180af90b00e8e322e8d67f00f1771d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784bc236edbd8c76f14feda1a5847623fd8ad5e8e64eaeaeb018ccf4dbd00fd5`  
		Last Modified: Wed, 13 Aug 2025 20:18:44 GMT  
		Size: 89.9 MB (89918238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a310721a4d23f498f114f679aaec504544e77a0451d6faadd40be7fd6995253c`  
		Last Modified: Wed, 13 Aug 2025 21:53:16 GMT  
		Size: 86.8 MB (86822094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514005321c7dae926c02aef7bd917b2b0c5f633908e5e3b3909871e125a080a7`  
		Last Modified: Wed, 13 Aug 2025 21:33:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b49dde360a060d5a271d7d16ba02acd66034ec7cf049f6f6f3017e33c73dd`  
		Last Modified: Wed, 13 Aug 2025 21:33:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:4e8fcdab0c5f477a5ce83d137cd9b004d62c54d81eceefc8947dc6836c6944d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea6255a9bc535de9a202398e47340734c65cdeca0ca1b1c6da0b5d16f3c178`

```dockerfile
```

-	Layers:
	-	`sha256:854759a5d72812a43f6bbd116d1f57be2ddb220317e35aad2bd5576ad737a8c0`  
		Last Modified: Wed, 13 Aug 2025 21:39:01 GMT  
		Size: 7.3 MB (7326114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b85d2d942d67760c09019b60466b62a6935105f599ca3432b44fb2cf6c4e4abc`  
		Last Modified: Wed, 13 Aug 2025 21:39:02 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550` - linux; s390x

```console
$ docker pull clojure@sha256:d9bc56bd29b01787a632e35ea8318541c67889bd19a7a9797f7660718edcf3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212180366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f564405b24108ec7ea8fa9a701baf72a29f013b5e47edcec3ebdafb6eb7c3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ea1474a78e77ea2d282f13dd08be3b8fbccb04451dd0cb1dfb115e66abc8ac`  
		Last Modified: Wed, 13 Aug 2025 07:26:11 GMT  
		Size: 85.2 MB (85226398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568e2b5e9c9c041b9eb37a44cefc6673532ab5c72abc334ad7fded14353f023f`  
		Last Modified: Wed, 13 Aug 2025 07:29:28 GMT  
		Size: 79.8 MB (79803060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffbd87ec4c952bf96bb763f0885ea9815d42aba840c6c1c9fb982392049211`  
		Last Modified: Wed, 13 Aug 2025 08:19:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3974c69e029ef8056180ed0156be6fe5b7de4883518ae21c2d6ac40cd56fd6dc`  
		Last Modified: Wed, 13 Aug 2025 08:19:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:8faa00169cc6c18996eba7af18090ffa0e21e019f44b73741c57875a1a271496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf624c7fe9bffcf652bddeb127da5afccdf905e460674c936ae6c1bf978ec3`

```dockerfile
```

-	Layers:
	-	`sha256:d523d7292369a69d148cb7253d49917f755a8ed8bf2481779f16737f25345381`  
		Last Modified: Wed, 13 Aug 2025 09:38:20 GMT  
		Size: 7.3 MB (7313467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7f147a5a65f658adf37d3ce6a2f6499be6ee4fae2b6c38f1a0cda3ad69ea92`  
		Last Modified: Wed, 13 Aug 2025 09:38:21 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

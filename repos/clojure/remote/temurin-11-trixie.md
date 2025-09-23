## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:23525df555079ec8c6ac3d493afff62608404be5625f55d0324633e23b4d1d2e
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b248236a18c2f66d945580991ed3697292049d40332c9dd9c29fec87d6f36120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280471036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76220b7b092c88aff1c35d6969e5a41aaad2f21dc73f6e71df57759708567a9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1861f7104a8483324f4fcc58ba0619908a1df84f62d5a34c395ffd504312a503`  
		Last Modified: Tue, 23 Sep 2025 01:43:24 GMT  
		Size: 145.7 MB (145658278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9215f28b1fffe51ca88a5054eef65938ac151f7febfffd8177aab8391901`  
		Last Modified: Mon, 22 Sep 2025 23:45:39 GMT  
		Size: 85.5 MB (85532580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3a64f264aee7d67d667cd64c37c6a0d3c1ad8682e9132e5694528e44ce727e`  
		Last Modified: Mon, 22 Sep 2025 23:45:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a1982ba4129fe862caf6efbfa641ca6820cbaf2e35014f7970d178cc3f146e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc3a8b5a0704ce2e0cae6cdb1960789ee44402d83f344d8b08520c11ac92074`

```dockerfile
```

-	Layers:
	-	`sha256:f62de23d86c93928cf024afa61bcb6e314d8efdf4384a7322619343aefcdce86`  
		Last Modified: Tue, 23 Sep 2025 00:36:43 GMT  
		Size: 7.5 MB (7486986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22cca249620e507389b589fc4655c5b247bec71a6f6ca03a9e4e717148e5e8a1`  
		Last Modified: Tue, 23 Sep 2025 00:36:44 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:503a47cfcdddb6e1654cc2c0cc753e7740090e2295518b71dd8f23202182e9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277461649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b061b716dbaee79a90f25daf94e341941fcf369fc6179fb386d769e6533db5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1adf3903c6969676ff7c123b1b8c99031b5872dd27ee07abbc153a60d4d9f56`  
		Last Modified: Mon, 22 Sep 2025 22:17:51 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c5c0f4b72c350288f679b72954e8e5a96ea9815d80088b1c3075c8f686f7f`  
		Last Modified: Mon, 22 Sep 2025 22:18:13 GMT  
		Size: 85.4 MB (85358501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d55616fb3d727b29c8703a0a603198118bfd2d3b0873dea5083197b0094a54`  
		Last Modified: Mon, 22 Sep 2025 22:18:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:63a335ccb0df4c7f54065de771c8596e20fe69a0f0bbde7261dfaddc8dcb7459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b82de91817e8cd426ca140904a9aea3c2dbc678ae70635c86275eb6a12a2f1e`

```dockerfile
```

-	Layers:
	-	`sha256:8f922f886bec3c37e91c35316330fc2953aa4d1b82e660f15910f2e2250211f7`  
		Last Modified: Tue, 23 Sep 2025 00:36:50 GMT  
		Size: 7.5 MB (7494634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b8176b49d700352e3e893f364a1ab3be30d09b10825cb00b5d0cac9fcb9583`  
		Last Modified: Tue, 23 Sep 2025 00:36:51 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:13b0284af8878c395d01c7da9da1e81aad491ff39c2b5b6e10b1b12e87fbce53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276912331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab61263b764f0808e6bd481c42eae749b6e97b06c2e2efa81df55340f27447a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b0a49034211a206c4a869bb1c851bf9118c29a9e0e9111ec6121f03fc6bf1`  
		Last Modified: Tue, 16 Sep 2025 00:46:41 GMT  
		Size: 132.9 MB (132852793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717274c2b7a789cff9ad672251c15720196631d216fe1dd00ad4ab279d98848`  
		Last Modified: Mon, 22 Sep 2025 22:55:15 GMT  
		Size: 91.0 MB (90954459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6e8644131ec0a7acb1d3bd48ef1074a298287a53f5aa2ab700d49644a6b3df`  
		Last Modified: Mon, 22 Sep 2025 22:55:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cc73ce8f49b9aabd76ad600d479d787dfcacb49a0301aedc69889059f7e070d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cc9e46d5de13bfb7c2a638f4ab3272725330de218e8f8995bc828c6eada8b8`

```dockerfile
```

-	Layers:
	-	`sha256:6fd81a14d24089d7c30e067e87d2e5a82869269b2ec45fd902271a21522d5f99`  
		Last Modified: Tue, 23 Sep 2025 00:36:59 GMT  
		Size: 7.5 MB (7490790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85a255af9b39e1ce43533522af9fdeb73d4471b72981a50b7e7d5f2c1dfccd3`  
		Last Modified: Tue, 23 Sep 2025 00:36:59 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:20714f7ed6b5da9dfe61f4b237ace5142526d5746c38fc410150b891dfa83e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261478038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9299a65b53467701523becf339231339c928c540948f73bb168d521a0bed2fd2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2a446abfc4ceaf851423ffb0aa8e8483550cb28f8220103fc82e136b37a81c`  
		Last Modified: Mon, 22 Sep 2025 23:10:43 GMT  
		Size: 125.6 MB (125622231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4494b4c4494a0331c562a3865b5c776f8759ef4070d173715724339b0cc43081`  
		Last Modified: Mon, 22 Sep 2025 23:04:00 GMT  
		Size: 86.5 MB (86508835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f86771b5d1c23a51cafe6815e596046f00e280565a251d0ca6907eb3e1ce562`  
		Last Modified: Mon, 22 Sep 2025 23:03:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:73659bb5bc0612f9ab425759c576236408098c24e5d57f4b93780fa15357e49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c88eefa757e8a567f05f8c792854076f2fad8f04518fbc7f3a97d1502dce7d5`

```dockerfile
```

-	Layers:
	-	`sha256:124402de8ed7b71bb91515fc3d797914660ec353e56c0af37484841b6233801a`  
		Last Modified: Tue, 23 Sep 2025 00:37:05 GMT  
		Size: 7.5 MB (7482912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077b664f1ebb7ae523b00d034087727819dfc01c249e1b5f6e849242f098ed8c`  
		Last Modified: Tue, 23 Sep 2025 00:37:06 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

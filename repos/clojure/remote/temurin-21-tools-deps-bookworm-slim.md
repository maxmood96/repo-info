## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3aacf6e94992356daccc4142281a4ce670fbd4c3bd234311a2ef8ad9e16aad19
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70d04543aea1858b3c436a3916c2eecedc43f66bd5437d60cd5def97943fe51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255793275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1253f203a336125a00e6d001f6430816b6afc790a6a1f9b95cb36e085c3593`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:44 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d642df67098049022300acae5cfa7a17f3e752dd1ddece11e6a7d2e468967ac`  
		Last Modified: Wed, 22 Apr 2026 02:20:19 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fed25d115f731c341af9cd142e0af14b7038c6181f95c07ac52acf772055e18`  
		Last Modified: Wed, 22 Apr 2026 02:20:17 GMT  
		Size: 69.7 MB (69698924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcaedf5bb48b348269fdd1d0adef9357f6cb9c8c4c10a8b4fe7070285195c05`  
		Last Modified: Wed, 22 Apr 2026 02:20:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e47b55e1c40bcb5aa54f6ee9cb5d69dc9ecddde52db969e6dcac9d4f8bbad`  
		Last Modified: Wed, 22 Apr 2026 02:20:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:619bbf0daa7ab0c31f24f7c7348bee6d4e586fc0516264c61bbd149d8e8e7d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe346da2b7903936d04f7361bc0d173f18bfa9f7c9e0b2d1b642782e62e979c`

```dockerfile
```

-	Layers:
	-	`sha256:9ca3628aafacd7b17d0957192dc078b5c22a6bbefebbc1f882c4c41c1a4d31f8`  
		Last Modified: Wed, 22 Apr 2026 02:20:14 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e748827cf4f71a04b19c66fc5694905e77a59b00ebe6ca6553cc162e1ef5aecb`  
		Last Modified: Wed, 22 Apr 2026 02:20:14 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d70f9e7cd1bf4827df6d2075534f8364151ad4767c7c2ccfc0a10925f40e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253942718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938a2c845466e2cc03e4deee6109a41e7b0eb25af6a4b62b9fd26c78b8a397b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:42 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8759edc74fa1b779e499901f463d84f0c84b2349979ccbc3b9fd47ab70a9523`  
		Last Modified: Wed, 22 Apr 2026 02:23:22 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b9e0cc0f11edc1711863f0d3c528a76d845780f80c6f08d471c793480a7a37`  
		Last Modified: Wed, 22 Apr 2026 02:23:20 GMT  
		Size: 69.7 MB (69692498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f75ebf496d2565bc9b8f33232d4cad2c958aeee513f50268cf16d7d2a4f81e`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe01c5808b6e755b92e72c39de6859be047266bdb4cc92416888d22292ce0b`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93212b00e811f13d20af4dfefe27e4e258cab4c00af1f0aa86fca2162571c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ea7fbb1babea961177a51c2188cb18e32767a8e05eff5712decd5fd5aa7925`

```dockerfile
```

-	Layers:
	-	`sha256:116238aded8b0b4583fa00d13f67a9cef8b0b2bb2584b4a52cdfdf570de37db0`  
		Last Modified: Wed, 22 Apr 2026 02:23:16 GMT  
		Size: 5.1 MB (5123780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a58454346f1893b8e228f0fb86775761368be37ff528b2d413450c002b77ad8`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e95cb6d9f24e253fbe83b3bef0dc63f16db15ab9f2a6e5ce37b777d3309f3d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265586743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c730206f6df3256325f368e1098da06e2a4508740a244f976fa88526c23b5361`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:37:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:37:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:37:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:37:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:37:16 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:42:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:42:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:42:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:42:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:42:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74781781a8a3965fc6776136be0d0944382d3635cb2eb0847cb27f6a92de98b8`  
		Last Modified: Wed, 22 Apr 2026 08:38:49 GMT  
		Size: 158.0 MB (157977486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2754004d317f84a36b799453f10aeccd233063b856e9dc36115fca0d36b1376`  
		Last Modified: Wed, 22 Apr 2026 08:42:41 GMT  
		Size: 75.5 MB (75529813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e12b460fff0e1fb0ed1152ace9975b2b97a0c608caa2ddc67736d8c9bf17ee`  
		Last Modified: Wed, 22 Apr 2026 08:42:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a9957d0131b7534cef78d0c0280fa2cdf87b25fdd88bec463f6ce31ece7b2`  
		Last Modified: Wed, 22 Apr 2026 08:42:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3731aa8d4629ad79e7f510662e9b7204f40956097860360b56b29ff4f6a807db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8c8425c8da609f1d49abbe450175c0d4fb926be14f5d739681dcea3e5b47c`

```dockerfile
```

-	Layers:
	-	`sha256:50d809f73d45b0ba03c6d1747df232ad55e5d6c5c943bbaa99349167e9350e63`  
		Last Modified: Wed, 22 Apr 2026 08:42:39 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee870bc0309d5a250a00f8d46239aaa00d559ff936af02499a9337e1446e5364`  
		Last Modified: Wed, 22 Apr 2026 08:42:39 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6573373a15813f478954bb50d32d5aa30bc7c31fbfa10c071196d7837cacbca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242510853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752090986452c84be4769a08629b70971f8a0635d61337c508f70cd603195220`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:03:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:03:03 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:04:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:04:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:04:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:04:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:04:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d069b53a2035ccac2b1dbb1b89e27ab2bf4d9e50e2e3be41b5c021b21dcc2c`  
		Last Modified: Wed, 22 Apr 2026 04:03:43 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451daca4619e5c26677f285dcb929a4cb7ce91e36bee4d1adc689ea516856a6b`  
		Last Modified: Wed, 22 Apr 2026 04:04:39 GMT  
		Size: 68.5 MB (68513039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159008f5ffc178fec84e412d2d09bb875c0e15ac28a8d07914c5d869484bb573`  
		Last Modified: Wed, 22 Apr 2026 04:04:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5042d9f106a842c1b721070f7e5882686d04608538275b65f772ad961d93627`  
		Last Modified: Wed, 22 Apr 2026 04:04:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb3cdae69b180b17af97fc5c704a8b6ac30d53b75c3821f7c15b4c4decb94b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc267f20c30937e48f22c36252ca55cd04c58f3c5f1736e8232d5aba4dccb97`

```dockerfile
```

-	Layers:
	-	`sha256:a794519b5089ee72f67ee85d9e8ee2e94f5e3eef8fb3eb320ee29118b6a7db09`  
		Last Modified: Wed, 22 Apr 2026 04:04:38 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10568a9d72a366c3be73d50df2e790a72a423d1dec0874b8f69d19d544dc8ff5`  
		Last Modified: Wed, 22 Apr 2026 04:04:38 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

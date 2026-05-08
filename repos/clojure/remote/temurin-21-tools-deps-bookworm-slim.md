## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:583541f98850604fc052da8d4b155adf5746e385817e69e1fc427b082509a8ff
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
$ docker pull clojure@sha256:6d0ba62c4b18a1943e03ca8db761930defef6b36a8136af32ae129cd4f408a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254270940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90438ca799d2f90025421b36a7952071ba25566be2928de1ab60034c099daedb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6badff8b9b46adac2cc2e8d4a5e4989572eb70344ecf613b0fc73e33ea382d`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 156.5 MB (156461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7099a19ae42911dfb0ebd622ed48d25029a661253ca4164acb1fe31381014`  
		Last Modified: Fri, 08 May 2026 00:27:26 GMT  
		Size: 69.7 MB (69692560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f29210673221f725721dfce462ace436925b2288524656ccc8a636346a811ac`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d74e810f03a6993c3503f85112bfbe0cb3f960c269b7310d9e6de474b5cd1`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8cefc62e391b490fef42594431e6ffaa47d8f93290f72a4d307d2c4ed4bb0619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2682375245d26cefdc02d365dd9c8539dfd0bb4cd8f194ee3615c5a37791810a`

```dockerfile
```

-	Layers:
	-	`sha256:f0de446f90b935afd17700c6ac3b654daf6c19bf81fb0fc29cbc259b44fd3d44`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 5.1 MB (5124407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60545e3928ce164588850f094ec307e0691cf4eb2b9b78d8d5818dcd8cfee59e`  
		Last Modified: Fri, 08 May 2026 00:27:22 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f35f50f26a116a2a08d1b5b394687db4a54e61fa97cf56f77f6278e8015f777d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265952469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e7f788baca6c0c1a38cde40604310827df150f2c0a83fc81ed6b132d690deb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:36:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:36:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:40:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:40:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:40:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:40:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:40:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030929f85e28291d6f68f9b323b1a7234dec490966f0e6af5276563600fd14f1`  
		Last Modified: Fri, 08 May 2026 01:37:52 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4c649dbfd5874fb49573edf84abf3545338d12691d37a569cad388740ae02`  
		Last Modified: Fri, 08 May 2026 01:41:20 GMT  
		Size: 75.5 MB (75529746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea4d0f9c8ccf81385714840b40457056a9c7fb0e533520ba5348cb37d8dfd5`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d4e0c8e3e411f236b2aa567d8d1621464a527a75688f57d97c0f1134521982`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cab38418b9b2283d77f389b620b8be7bfd863dd611911ad3c724be8010ae950c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b326d5410337da71971c58adbc2971c0d0508df4471664ab6261497095698c0`

```dockerfile
```

-	Layers:
	-	`sha256:86d43a25ecd68073b12ee2799624dcdf89167e0afbd9671267c61ee304cbd380`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 5.1 MB (5123804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d8b43923e135e94982b50bd02c6e3ab9457ff04af59c4ac149739b6da9ec1b`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 16.0 KB (16038 bytes)  
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

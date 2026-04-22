## `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:b2500c81d17bd6da8621817e6e469bd934a829f6fc933c119212a1b36a0e2d7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aebe3942a7027ba3db02d8638b5b7c8f1d67296d285895d0bff22c1461fbc349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153105988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8703fc4e53043c6e1cb21cc3a8af08a940774a38f74dc59bf4eb1c0bebcb28af`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:15:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:15:15 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1eff77e6a51c17b6e3a08fcd3a36c13d776376f3c2df207e788ca742c27b41`  
		Last Modified: Wed, 22 Apr 2026 02:15:42 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2559fec94ac7e6b1709e2ff6810d08cbe026a33551fecfe9600f5cd213fff9`  
		Last Modified: Wed, 22 Apr 2026 02:16:16 GMT  
		Size: 69.7 MB (69699031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0326e34e4cd2162cce4567026c89e4c669fd12dbebf41279626e826a4eb3387f`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f624fa75244f5e50f65f9202523b08f660008354ddbeedaf12cbb014e668b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc8cfbc2491f40c4cb80f1682daf6941f41f8d133073b500778d7bc3d72ad36`

```dockerfile
```

-	Layers:
	-	`sha256:6d86276228bd3c1fa6888e169195fe50d014872904e0dce11d3726d284e4cb8b`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0feadac2efd90d4f42670f517dd7e96022ce36708a60f4d18641aefbb7e6875`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:555d207275b59a765138f9daf74493bcdfa48dae5a85e7a48ecb44ddea5d498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152060940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab1b04c93e92790aa2ae9924567f818c5d16e8104f8da9c45bac9b2d4e7e2e9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac91cdd85102d1953a604e0d67f5d00c6ec829babaf3b2c1e0ec8e06f676be`  
		Last Modified: Wed, 22 Apr 2026 02:20:07 GMT  
		Size: 54.3 MB (54251620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59200be205125faa38d9e82731b59342b0bab6d2ffdcd158165d2fa79884a211`  
		Last Modified: Wed, 22 Apr 2026 02:20:07 GMT  
		Size: 69.7 MB (69692561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57898dfb882d85f9d19ed5b58a476200d7b0898a0f70a65411f68eddbe93cde`  
		Last Modified: Wed, 22 Apr 2026 02:20:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3dfaefee72ba905616a8c604ba400cc520e06e3bc923eda97d4ee4a0ca0a2f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c514c850caec949a1be2ccd0b53f35623b586473eab46db5a75bd61e8906ebe4`

```dockerfile
```

-	Layers:
	-	`sha256:400e95bc415a1c4880997f717de9cd0314fdd47d0908df1077375e7a12bb9d9a`  
		Last Modified: Wed, 22 Apr 2026 02:20:04 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020e46689745d4bd771ecb5c8e31acc52bf480c3650a3d14969dd987dd3705f5`  
		Last Modified: Wed, 22 Apr 2026 02:20:04 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e30018fbdba3c26c676e25d30bf8afe3c8ad8d0597f2e07bf697a06a3f0424d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160259273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9fb84a8e6d7d6b6b47639e501cf0e78e751f6622a681c95b0c92aee0643f4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:31:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:31:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:35:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:35:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:35:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca09ab2f7ae5f0a2c569e6862baef7188079f93d19533ec83941e939b63131e`  
		Last Modified: Thu, 16 Apr 2026 02:32:47 GMT  
		Size: 52.7 MB (52650382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c130019a3cce2cf5187302cd0102edb21e6071d3c123eb8915f188bdee2ed`  
		Last Modified: Thu, 16 Apr 2026 02:36:27 GMT  
		Size: 75.5 MB (75529781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b3378a4fd945a07400d62324ad5385d9df936b11841ae0e8fe4c4d9160fa3f`  
		Last Modified: Thu, 16 Apr 2026 02:36:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5e3bcaf3034ddde9ab1793165081e5af87a893418f208bc43c5973ee54ff2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c763f924b74cb4184ff96b5c90ffe722bca3c228e054639cef94cc18fb8a98b`

```dockerfile
```

-	Layers:
	-	`sha256:384532cb4d0be5afedad9797b33cb068db7c9cd14ad694a41322b24e82dab057`  
		Last Modified: Thu, 16 Apr 2026 02:36:25 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ceac58de47a2e3a0bb1a7d46607bc03ba0b2273b2488dbef4f07a64db98986`  
		Last Modified: Thu, 16 Apr 2026 02:36:24 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

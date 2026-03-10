## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:02b4b8481d602900113f8f6be0eaa89b38987cb4b5e8f862afcd409b38d3997c
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6ad598d62fd7aa9d4c6c3629bd366e8adc24a977263b102e63be771faf4182bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243745148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ddfc96f53decfe8752026b75132db8134465ddeeba333cc4af348202879f88`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:21 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb15e87fe83382cd76367750035e7fd370d7bf5fb4f2e4573ef5653f41913498`  
		Last Modified: Mon, 09 Mar 2026 20:34:57 GMT  
		Size: 145.8 MB (145806702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d671f012cd7e328b373e8e161da05d5472c7749fab88c1a72ba0042404147`  
		Last Modified: Mon, 09 Mar 2026 20:34:56 GMT  
		Size: 69.7 MB (69701522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5f284249e78e2ae7a28277dfe4ec880c42fb95f40b094c7afc099359d2dc0`  
		Last Modified: Mon, 09 Mar 2026 20:34:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:593bb590f5c365566e2b6c3a9d44034b82b17fc366efa5b54f51a25445a8b24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d464d2497bee155d362ad3e77cfdd25576be6e4002698e1c7545acb0fc7931f`

```dockerfile
```

-	Layers:
	-	`sha256:841369a3342b47c696988cd034f06b753af62fe4ed3d6b4255af65f5b84ee2bd`  
		Last Modified: Mon, 09 Mar 2026 20:34:53 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7591e5abe6e24749e83d13ad14679d0afb519cec9063a10752acc3996479dab2`  
		Last Modified: Mon, 09 Mar 2026 20:34:53 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0958a1f9e0f931d20d23a9e3180d53bc274847ca3f80f18773dc23a3060e3d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240307048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7eeb4cdce72d39067f8591794d6fe1c5230f51f0da8adbfe07a8eec89be20e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:16 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba53cba111807838674ac4eeefbf505a8148be7b58651d573c10fc4e86643cf`  
		Last Modified: Mon, 09 Mar 2026 20:34:54 GMT  
		Size: 142.5 MB (142501424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebce70e9e46fed441e1e4c7ddad29247d09007b158aaf33adc7d3542bad762b`  
		Last Modified: Mon, 09 Mar 2026 20:34:53 GMT  
		Size: 69.7 MB (69688897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f87932b2c0bf4b50d569cd27d4b768713d1db622d3c24ced8f4a93e8841a86`  
		Last Modified: Mon, 09 Mar 2026 20:34:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:891aeaf26cbf3c0995dd7bd581b5c7895fe2e2980b64bac101b6e9e7f727817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ddf97862c1e57c743192ae941a7c27fa7bf2e9507afc15bbe3ed17eb386947`

```dockerfile
```

-	Layers:
	-	`sha256:7d2f2df31798a302738642332cbb06449db95e9a69a8b7ea1e1c5e9950923a1d`  
		Last Modified: Mon, 09 Mar 2026 20:34:50 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7276d564a5891705b475dc48e1b96fee9d6e1293719f806d1eaf3348263fcd9e`  
		Last Modified: Mon, 09 Mar 2026 20:34:50 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:89066c87df3d91e93e24dd37c3d31462cbe3d799abbaafbf67ac25a8563fca72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240610225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaac2c212390547dd7cfae139e1f69452715a34682287af8732b229c20256863`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:46:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:46:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:46:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:46:09 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:46:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:46:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:46:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07635c2a81b963c59cbf4e59ddccd52bfee62c195984683505beb6f3aff0b8fc`  
		Last Modified: Mon, 09 Mar 2026 20:47:34 GMT  
		Size: 133.0 MB (132997797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de96a720d12f06f9fadd7af40c23312c705ed75aeda3fcd795bfd0f8498f1da9`  
		Last Modified: Mon, 09 Mar 2026 20:47:32 GMT  
		Size: 75.5 MB (75533449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d88f340ad4cb5c6d70c760d0256d56c3c75c47c965fe068ecaf0fe0a8bd23`  
		Last Modified: Mon, 09 Mar 2026 20:47:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5df745b09e847fee79d8861c47ac9de7e47d4fae2b7751432d340ce87407d839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29cdf50f2c1432f0fab576312617cc031112c7b15d3d181b8eb9b873ed8d7db`

```dockerfile
```

-	Layers:
	-	`sha256:407e8dcfd71bededdb56a659d5f0f29da370a667df2bd867b4a4ac7fe9d57a41`  
		Last Modified: Mon, 09 Mar 2026 20:47:29 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b466036632e36d0384394301c9f20d8ad38bd6546922235c6a27509e6822fdc`  
		Last Modified: Mon, 09 Mar 2026 20:47:29 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:73357869a4719bfb3b3ad868c7f515d1e96c1f18629212059e6bbd50247c4574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221967994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa1e19ede347559fe477df8b0a8cf3fb83ec0e3d36da9990a49286fed6e1995`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:32:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:32:13 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:32:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78455097ab053fd4a095369b6037e8270ed42dee2c12d398c3ce66f2d955316`  
		Last Modified: Mon, 09 Mar 2026 20:32:59 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392d179574653d939612370537b737ff49d307e01bec020c02897eef0748c35`  
		Last Modified: Mon, 09 Mar 2026 20:32:58 GMT  
		Size: 68.5 MB (68513764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cb70fb717bfa2edb74de6384e733afdc2169bb09b9dcb16b261d5cc1893ed1`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:102c31d548276908d643b2b57f869e5b052884b6cc921e50750ac48d994678f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b03617c7c3a02987b5573b1be9f18e0265dc48d93503f4a9e54d3e564ebcec`

```dockerfile
```

-	Layers:
	-	`sha256:28bae32112a7a48f11adaf5c39262ba36431376b2a9ef42912ad2b285305a5ae`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac683156d89805e4b153812724d649cc8617b1d01d55ebafd1524fe3e672e593`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

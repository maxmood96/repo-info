## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:e5bba647b2c9bacef103c21c63525416216044790c15bf5235b16737e219467a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d3409bc4484604666090f80fa1f5217379ecde7801637747f62c3952413708bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156961843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2c1be33e78607904c7e9deb339c226b8fbeedf0351ad916fb4f76d59f76dd8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:14:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:14:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:15:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:15:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccdef7fabb39dd70415cc8c478e12177bb0aafa382caa609019002bb7183c16`  
		Last Modified: Fri, 08 May 2026 20:15:24 GMT  
		Size: 55.2 MB (55170085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da559c0664683a6f8900f846cd738c6659fea8839f70f22374896c04997e784`  
		Last Modified: Fri, 08 May 2026 20:15:25 GMT  
		Size: 72.0 MB (72010887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82f53706f31dcdedc4aa240f14726f6bb94873deecc5bedaf0527a9aa86610`  
		Last Modified: Fri, 08 May 2026 20:15:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a37c8a6fddee0f7e243659d75ac1436bf4134155572598c7007f909b97d8a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c54aadceb8c6ec7ab41db4a7ecf13fe170be5ce137aea2d37aaf5dcc0629258`

```dockerfile
```

-	Layers:
	-	`sha256:e1c6fbbe03fa244bcc00ca1393126df8818c27f8385163303321a831a623d001`  
		Last Modified: Fri, 08 May 2026 20:15:22 GMT  
		Size: 5.4 MB (5380179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c0411b77277a1aaa6bd012ba0f7c78c4b81caa14054c15c44cea112cfd899c`  
		Last Modified: Fri, 08 May 2026 20:15:22 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8285b068a5919e26d0f34ad82b8d2aa5acd01f2076392f307af5d92278a1d06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156227479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb6e311d3afd46c5a9d66e4b464adc5ff5efcdabb2dec445d8e316f97fd4802`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:19:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:41 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e143e9d238c394a39fa16273882f4f2098d5be64145cf5ae6881367a56ec44`  
		Last Modified: Fri, 08 May 2026 20:20:17 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e8c15ff3303ab7b5bf69ac40aaf9a6ed37919e351fc60bd006575b5ced60`  
		Last Modified: Fri, 08 May 2026 20:20:18 GMT  
		Size: 71.8 MB (71831576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a9856f381c56a325ffdbee23389e13e60bedab9958571a796fe3edbbaf2a56`  
		Last Modified: Fri, 08 May 2026 20:20:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75383790296a102cef2f00cdb0b50ed687d28909cfc76474841520e25d16170d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3427e6d8ff038570801fdfcdcbbe7d5ff851dccce0e60b7aa65395ba6a9e7`

```dockerfile
```

-	Layers:
	-	`sha256:36180139347962164fb4e5365d9e0d7d217efde8ec23a7cafd57cb1259b4cc77`  
		Last Modified: Fri, 08 May 2026 20:20:15 GMT  
		Size: 5.4 MB (5386648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c622bbc7bc55721cddb06ca6dadcf402f594dfe4ec735fff226d73c617e4ae18`  
		Last Modified: Fri, 08 May 2026 20:20:15 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:acfb46e07f62ece96a2c337e3382bbb811c12b1cae22530fed90fcd3794d9801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163677454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95b748d55adb5b97916f1d1c48daa13436066162f738bc4fe14b9aac431a88c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:16:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:16:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:16:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:16:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:16:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:19:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:19:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:19:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909dacfd29690d1229d823bbdff4948ce65ffd405125b5cb14537992f61a0959`  
		Last Modified: Wed, 22 Apr 2026 08:17:19 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f0c74378f2b29f7d9fa383a3cbcc484f21fc13e9a77b3c29d6d74c784ae14a`  
		Last Modified: Wed, 22 Apr 2026 08:20:16 GMT  
		Size: 77.4 MB (77428387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a539cb8410f6939bd9d31b654e493435300a31d4717968d1ae3b15584cde6`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:384f5f811c780240d0031972e2facdfb3a75a06b2f97aac5e67bc6b5af028f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f723c696e988d8bac469db7d55c2f5641a05d28b708a57ea9ec3576826a07add`

```dockerfile
```

-	Layers:
	-	`sha256:fabebc9ab7f51a545ee41a9d57c6d0f53e6596de3c5cd63455d07ff159a3423f`  
		Last Modified: Wed, 22 Apr 2026 08:20:14 GMT  
		Size: 5.4 MB (5385145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970b1fc2a9b2eabe8cfb73b4f3b67a8731b65298abe2f0b2f79162b0437a31d7`  
		Last Modified: Wed, 22 Apr 2026 08:20:13 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

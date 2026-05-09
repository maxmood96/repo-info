## `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:8168771c52ba9a963dd1cdc2b771d4b26bf5a24236ff9930fc42726364b0f047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ff76f438d2507cec93e2e55bcc1cb2805201a609f0f50480f146967d0afaf419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163677694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375be4dea5c18532c2cfa172ac1ec67a59cec7dffe966cf744e8f5c13820aded`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:21:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:21:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:21:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:21:53 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:24:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:24:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:24:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3a464c62b9ffc5fd94abfa0271a623a6da1b008cc9d6c7a1868743f509acb2`  
		Last Modified: Sat, 09 May 2026 02:22:53 GMT  
		Size: 52.7 MB (52650379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982413528f61391ff43d4da5f6bc47a663386134b6b5386bb7a3612f1d5d3e89`  
		Last Modified: Sat, 09 May 2026 02:25:21 GMT  
		Size: 77.4 MB (77428584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7007b68e6529413fd5bbfa92be1e77b376d50b0117455e84c2172c628db4c93`  
		Last Modified: Sat, 09 May 2026 02:25:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:383b118a2a22848f522017dd2468a30252ab7337c153167316b9f929d6c15569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9905085f57809154e22f56b48b05a2a490ece353eaa37165e4b41e068beb2c6b`

```dockerfile
```

-	Layers:
	-	`sha256:059c7e25e413bb3fc5b19e17f4dfac6a6bbd566ad53b4d37c7b8ed04516a88f1`  
		Last Modified: Sat, 09 May 2026 02:25:19 GMT  
		Size: 5.4 MB (5385145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783b73372884cefc884c31c09034111a25f24017da1e5821ea02b9074eb99c4b`  
		Last Modified: Sat, 09 May 2026 02:25:18 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

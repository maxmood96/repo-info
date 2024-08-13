## `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye`

```console
$ docker pull clojure@sha256:70afa601042d897d342f269e4751964e3adcdd0cd805f362877e53b1b3376e16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ada6702da600e347010370da476763ea664d542824c3f4bc45d0916349d89bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227659589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e440bb2503e01660e30f7aa9465eca37ff7edd0f987fb160ec2a4359437b74a3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ea8fdba7573bd1167c0b559ed2afec72121e88307115dcd4def910ff35e79b`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 103.6 MB (103611898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508a84777c6c3d8e8c18c2ad67755d9c8ba288580bc293b8808ec9a131da82d`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 69.0 MB (68962372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ce6e884ec4ca2c16a7a21511b93110c6c1becc6712853344cf361be267257b`  
		Last Modified: Tue, 13 Aug 2024 01:11:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1b4a26b619f2ea5d0f8c8a2e666a1964f04dec05477772cda68913b0088138b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130856ec5780b55df9dab4247bdd02e21409588365a1eaefa513bc916038e4d`

```dockerfile
```

-	Layers:
	-	`sha256:e0590f5534714db37db34abf23c891e9fbfcfab7affb57b9ef584ab7107d730c`  
		Last Modified: Tue, 13 Aug 2024 01:11:16 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3570f565b861dd541934affb919b28537cccca9e17a1066844f2ae9925ab53f`  
		Last Modified: Tue, 13 Aug 2024 01:11:15 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dadcdd2b472e0132a9777fad25456270f5306e726eebfbb1848487b2e11d6c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225553542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b36d225b1221b20b758e15106e94efa0444cb1ae343fdfa3073790c97624f49`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa99483c1e482a8add6863c8a0b9593712934759e22b2e7c3c82f4278324c6e`  
		Last Modified: Thu, 25 Jul 2024 19:09:45 GMT  
		Size: 102.7 MB (102729199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbd3d61e357b4eabd75b449e026389bebddd71b705611974694cf8feba53a8d`  
		Last Modified: Wed, 07 Aug 2024 19:44:39 GMT  
		Size: 69.1 MB (69093710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6c4979ae6ff1f5c91d5759a4f416027538e9cbce05f41ee2392effc3552d80`  
		Last Modified: Wed, 07 Aug 2024 19:44:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9e495ca7232a693b22b9f3f14a9765396248d084014f813e436042d78592e5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877ee7ad5d43286bdd20674bdb2c6b6f68831bb46af865d670394f9452ae2e4d`

```dockerfile
```

-	Layers:
	-	`sha256:684a4824e8e61611f0536f954a6ba44769a7992b5e62df7c8a26db2346fb067e`  
		Last Modified: Wed, 07 Aug 2024 19:44:38 GMT  
		Size: 7.1 MB (7071557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d164cc6f7792041651a528c9d4a5eb3e3ed299b1e14066441457ec340eee69d`  
		Last Modified: Wed, 07 Aug 2024 19:44:37 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json

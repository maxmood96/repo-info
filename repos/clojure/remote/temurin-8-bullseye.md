## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:2976943b4562fa379ab5231f958b09bf1c2d04da0f61bffb2bc41f8600afbbd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5e5b130aeb8075e0233418b03633a2d091fa6ccc8e2ee04966c66fb541ca82a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228026915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e81838eaaf0b78de8090490865b9c38cb011aa648fa75213f3bdfdaaf7a18b4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f0c9de5c0464a7016be502647b786c714fdc66534ff48040eee36e4fd6d19`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 103.6 MB (103611915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6620a3ba902d08aa2b7d54920ed08d376b06ce3544d6e20dd13f6629a99f25ac`  
		Last Modified: Thu, 17 Oct 2024 01:13:29 GMT  
		Size: 69.3 MB (69333746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0ab7aa6f14a2a759e45f186667aac5c9dbf5449addaeb7a16c2db3d88b506a`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c6cec573f34e453033b0ef24d05c87e9733337165d48ca40b8ab660ba66333cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bf056dcf7838ee118073f2d54e450d2d878868492b89ebb341f705f2036c92`

```dockerfile
```

-	Layers:
	-	`sha256:24850f67ab82a066253b132bec863445f7823ec68f0babeb03407f4eaf0ae32b`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 7.3 MB (7312259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d96161fb2fb9b73623799d8c23ffad52bdddfc608c28a022434695452ddaab`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d413ffec1bbbaec1e58d62769628c740c091cbd730601957eef92c80f8ba9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225931734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ad853443bbc41fa9b528c042eb16e625fdc4ec41b60c6b5b46d6f9a308859`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5868f60870b916a798345f277a75fa895b849585a3f923ed55eb1471eeea76b`  
		Last Modified: Thu, 17 Oct 2024 07:57:44 GMT  
		Size: 102.7 MB (102729258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26345ada33427b07cd8f5ac0c2a284be9d09a893b0057e192749860951a42d9`  
		Last Modified: Thu, 17 Oct 2024 08:01:31 GMT  
		Size: 69.5 MB (69466937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9863219f2dd7b535a578e1c03ac33ddc38a2f09d171d20f3388197ae274049`  
		Last Modified: Thu, 17 Oct 2024 08:01:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cb230de61ec4acbfb45ac01fdac33f9b11b4e35938e62f29793b6dd210fb9adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7332057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187f975ad9cd9744a8bc2ab1084abaea6d49e6da3bda0319441763759bd717a1`

```dockerfile
```

-	Layers:
	-	`sha256:db5065b7d3b330a5896600c1f56f9bc3c8d88896b586ec14e6194ffebbfcfdaf`  
		Last Modified: Thu, 17 Oct 2024 08:01:29 GMT  
		Size: 7.3 MB (7318061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c53ba07870c26f4543771aeb2ba139a7301d8d1f0b3282f4319c0eaff82247`  
		Last Modified: Thu, 17 Oct 2024 08:01:28 GMT  
		Size: 14.0 KB (13996 bytes)  
		MIME: application/vnd.in-toto+json

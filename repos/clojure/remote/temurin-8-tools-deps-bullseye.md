## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c282e8b4203f3c52115a723b75f7294428a9b9bd4e950d37bd839918cddef907
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:76d5dc07ebc6e6a293b074cea0b8115f669b5ba2264f3444023fc0e9a012355f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228026774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626f8060c62be818e6b65af45ae2c265c94c2594d13b404c3c90e14f7f3d204f`
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
	-	`sha256:d267253c9a938843266237fd5a9d4e8aedf113b06f077bfdbc031d0599ec033c`  
		Last Modified: Sat, 19 Oct 2024 02:55:25 GMT  
		Size: 103.6 MB (103611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc7715d077fc223afcf1c1baa50b1a9e06a83dc0de9e947b26accd3753abd9`  
		Last Modified: Sat, 19 Oct 2024 02:55:29 GMT  
		Size: 69.3 MB (69333608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0f9be216f93e26d1b224cca1984ab2ed1179504ac86c26fd04e9e58eccb977`  
		Last Modified: Sat, 19 Oct 2024 02:55:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7aaf371474f11d972148ec394fea94f8cf66a88c9070bff01b4e4b9d4820772b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65df5e485a32b42411ea23d9fda21bb488e309cf7f0ef023ba87513b830df10`

```dockerfile
```

-	Layers:
	-	`sha256:cbccfcacc5de3fc47b9f9e8c8c618da7cded198ff87ac6b2a92404e7cc51adc7`  
		Last Modified: Sat, 19 Oct 2024 02:55:28 GMT  
		Size: 7.3 MB (7338004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d0451296ee7f2f8a389f0477ce060f72b0ec42a2f5da409918f8cce952b8f7`  
		Last Modified: Sat, 19 Oct 2024 02:55:28 GMT  
		Size: 14.1 KB (14061 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

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

## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:fe68175a0c35afe7815f840cbf262707463844228032c46bb5a71e174920e9b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de47bd2742684151638ef141e437716f390be081c395064d2445ea5f68855080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234148358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbf3a4729046b00c79983db9046934abb87da147f32e728782ecb0e33f0c832`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b16c04b8f6610e712af885756fd98e57967888b9edf73edf4f43258092f2bf3`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 103.6 MB (103633891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c68e003724c2587778dab1ebc3619061532957a80106c791426cdc10bce55b8`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 80.9 MB (80938131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12b9eae06f9da6e37ade0f7182d8e55816865b804763fabfa679ef6b794cf1f`  
		Last Modified: Tue, 12 Nov 2024 02:22:43 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9a7bacae4fa476c7514ed3b1ba9c6e2d9f6cb23db4f58293772ea48b08e3874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ba1d51996ac1e9ee81e7f2c7df93058f9eece9c8d6a627fc495d03ac756768`

```dockerfile
```

-	Layers:
	-	`sha256:411f4981dc6778dbb66a1740b5dd9b01efea42f1b472cfff2d18091e6a8f3cb0`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 7.3 MB (7304593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ff125719430986dbbc79b1b63c4ebd34a4ea42acc626c952aa6da4d6c28706`  
		Last Modified: Tue, 12 Nov 2024 02:22:43 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a797e194c35e088bdb15af7bc961fa34c08c9deda7f63d45b90e3fceba0635f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233123699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01896ec5ee1b5b1735e02c40efe2ec327102037e06f8e7e1202688f177898cf5`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd8cbeb553b9ba577cbebce9c0f323243b8d67540a8791908b33d3e579a9fa6`  
		Last Modified: Thu, 24 Oct 2024 08:51:34 GMT  
		Size: 102.7 MB (102747707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e705abd10a13b5682a18521b3089d23b353ed9603b81b806d9e3134f28a4ca`  
		Last Modified: Thu, 24 Oct 2024 08:57:54 GMT  
		Size: 80.8 MB (80790368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9f4e0d16a07d11ddeb34fbbda8747e8d16554de90bee5f45f7f7a7128bba13`  
		Last Modified: Thu, 24 Oct 2024 08:57:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b9b9c6654b876411142867aaf4313b8099f0999465227df02a69872d361437a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7325197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209687325843124a5661d1e9ebba97f3f20af4b1cbb0249c8434dd940b27ad7b`

```dockerfile
```

-	Layers:
	-	`sha256:2501c5a480f671b88c65a2a45cce190afd2e76e81f53fcb52b59d1b97a9c91bc`  
		Last Modified: Thu, 24 Oct 2024 08:57:53 GMT  
		Size: 7.3 MB (7311024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee6ef93ae0dda21a8f28117370f4a42d588954d4603d56d2cf1c7220f7ec34e`  
		Last Modified: Thu, 24 Oct 2024 08:57:52 GMT  
		Size: 14.2 KB (14173 bytes)  
		MIME: application/vnd.in-toto+json

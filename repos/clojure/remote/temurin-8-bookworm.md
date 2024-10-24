## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:592023b1b44c8a0cdb2ebc751d0ad1170a641ee3858f3d46dab3857dab1c38d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0d0c4450a42839b4f69d61a3a7d5bafc0a4997ccd17fbf311fb033e173c22bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234117781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525ffa7fbeae7d2f4286d21d7d43f782babc5ce664b63be35f90af2089996b1b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050a8d88f91926616b290162fee02af713d55ba11227c31e5b5d88c1fcfaae92`  
		Last Modified: Thu, 24 Oct 2024 01:59:15 GMT  
		Size: 103.6 MB (103633964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ae2c52e712d740ee014c1eb5168c44373caf2177086461c484a3df5e7176a7`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 80.9 MB (80928151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fa266ee31109bd86a86082832ec8a399ed0e8d2f91d9b8ed1331d2dc3b662`  
		Last Modified: Thu, 24 Oct 2024 01:59:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:43a74af42829c915b674ce788c4f9485dc62d1b502a7b6973ae5dfcd2f7a786c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e886accd322ca8fb454c25134e804ae99f79731188f43ddf8099bc5ca7ef95ba`

```dockerfile
```

-	Layers:
	-	`sha256:d82df5f7ef1efc3818f287fd2230611f95750538ec443ab300224df6e170da7d`  
		Last Modified: Thu, 24 Oct 2024 01:59:13 GMT  
		Size: 7.3 MB (7304557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33224a4fe5016952b78b5bef762e76cde8728a924a8c0952c5a863b4f01f4eef`  
		Last Modified: Thu, 24 Oct 2024 01:59:12 GMT  
		Size: 14.1 KB (14061 bytes)  
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

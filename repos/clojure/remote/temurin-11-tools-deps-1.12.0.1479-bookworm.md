## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:16a7e03b5001c4b75481c647f9dff0444fb8cac086a7c95026434b30b0aa81af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:88602e042fe73be628597ae9834bc021bc501bec745d832c5277bc6415575a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276036073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137006e7dd871d54ec2fc893cd760cadcf5ba73a62c71aecf99243b2d585e638`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7094dfcf768c2c008049104c2a1534c7f356c2867ac1ed542f7eb461be07ad11`  
		Last Modified: Tue, 17 Sep 2024 01:56:49 GMT  
		Size: 145.6 MB (145550046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e745fd0975aa63807090c397328f0953abf322cb23cbce20702d753e79a40bdc`  
		Last Modified: Tue, 17 Sep 2024 01:56:49 GMT  
		Size: 80.9 MB (80928678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27f89f4317aa05bd441fbb2c242c1075b433daf64ee57ce5479512889d51bf2`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3d94f6351cbdda488d93b20f875f04c0ac821077a816bc26dc6b6ef2cacbd09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8596bfd96555a6102f4f68cf56c940b90b5acfe00dfde8b8862e5a94e3bf67`

```dockerfile
```

-	Layers:
	-	`sha256:53edd3d4edd5c2c1487496bd3d46dfa4b6aaac404af02ae8aec88cb49cdd4d32`  
		Last Modified: Tue, 17 Sep 2024 01:56:48 GMT  
		Size: 7.0 MB (7006987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02e09ac12b39f024bbe9a88a79ae26d9d12fe9faf48c452d66e87bc0d39a883c`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad1c6249a6339f6e4f1f3d5cfcb9ced6385430eff7ca56390b3356db4d1bfcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272731251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef19a93f537d7a45fc0e286d92c423e929477678eea95686abf165b2ae351`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3df7a0f576d2d0cf07728e3349cf460816062dde696437d39d2061a179a83b`  
		Last Modified: Tue, 17 Sep 2024 04:18:28 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875a6f1e310d9ccd79b78ceef8b0bc6d16a6497e1330a867eb9e4b82b5960819`  
		Last Modified: Tue, 17 Sep 2024 04:24:18 GMT  
		Size: 80.8 MB (80790166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1597d5fbdbde4e55710ef0faf9aac772c2222c50863580e825aa63c1de336e20`  
		Last Modified: Tue, 17 Sep 2024 04:24:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d68f06e411eeeb95579fa0abb4f46c3acf04e64800ecce59e24142f5ece42a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7027774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463df34ed22f9bae38fb224bd166022181b11b50515356ee0a5541178e5b5c3a`

```dockerfile
```

-	Layers:
	-	`sha256:e65d6e36112bfcdae71e0bc85bc9124ab4449800b7c895024157159475d297f0`  
		Last Modified: Tue, 17 Sep 2024 04:24:16 GMT  
		Size: 7.0 MB (7013374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55166c27319e7fd99d8370ed2c1ea5ca74ad66fee98f86056a88fefba1a9ed26`  
		Last Modified: Tue, 17 Sep 2024 04:24:16 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json

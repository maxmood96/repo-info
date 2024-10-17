## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:001ab487b2422a738a050f6ba703ad73fa6a258a0b7e2ad1adb9d156c3b04fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ea0007f677b4e4f4b0c5db5e36c0350a9ed37d8f22f202ffe27f23fa71598317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295751716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e1e55856d40c9733e2eda088ed455bf565f0f5f80f165b8f07b3e51db90ddb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68f122a48350ce95e50896724eca961fdb8235429755ef94bb4ebd2a551d57e`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 165.3 MB (165267630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2feb92f830c4f1b10ecde3eb2a6bd9cb1b7955aaf4af651aec01d79e6c525df`  
		Last Modified: Thu, 17 Oct 2024 01:13:47 GMT  
		Size: 80.9 MB (80928024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94580c18e453d533a6df4758784eaa7be5cd32876b4556b30ba4d2e1555c4779`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7475e678dd4a576d64a8f1ab5c4dba1c5510825e941722fa37fadf62b6d7b`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:79406cfdb0f0f038a0bf1e3739b29ce20089560ec47debf08a87b3dbdb12b73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6593fa6f233f79afa42f92dfb8f8566c65a17e58335b0ed8305d7819250e3f`

```dockerfile
```

-	Layers:
	-	`sha256:560410e180e9064b2cace656bc5075276de700650adde16a7c46c2b778eeea6f`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 7.2 MB (7162323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46800432b824bd30cfdf15c5c7511c39483fd3295c2881dfc399170570254fb9`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b50047c6c13d48a973deaa542b97482c788b395e86de2c87d72370fe142f1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293628876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1443e4667ab45c0fff19e759ced679093a3e875813928dff0a8b45eed71920`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72374e05c5fc01256ab2bbc23ee7744b5db54d404aac7042df98fa6ce9ce8f3`  
		Last Modified: Thu, 17 Oct 2024 08:27:41 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c02996c20eec70b7b6be0d70ffc26515007dc650ac86b317c732113f4f286d0`  
		Last Modified: Thu, 17 Oct 2024 08:32:36 GMT  
		Size: 80.8 MB (80790058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0573c624f92dd9292787ac2ba42af96d4ccfa47246e5145fa0d49b9bf81507e1`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c38732d38f1ffa6cf16dbc734e4d766fb150c311429f25afc12dd4d3ad342b7`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d01a1cd4d961e2e0288e95aacea50ba08452d7eb542d288005cb28ce806488aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045b867359975e217e54ce0704abf992cbaef7a7fb6958d39f77835771bc383c`

```dockerfile
```

-	Layers:
	-	`sha256:e1c33ee20bf653376ceca46cf6bc21cd982cac021d923510466b24975e234232`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 7.2 MB (7167493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388953cbbd6a3bff1b2e375fbb4b14563deca21455750874af28004367db3baa`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 16.3 KB (16292 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:0fe7b610bc058725eda0763da98c99b5ed9a7940fb3919741fe00f8e6e620150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a9e6ef086b83adfb8c4c8ca1cff8595b1ec864d575cbd99bf253ff8aeb49b5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271296779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0012cf134f4c087f598f35eb55e3dc8ffb7f24077b5f41b6f304afdafb434462`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d1829db38209e0dcaea7cede81a02a792e370d5738c2ee01ce49e4072203a7`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 144.5 MB (144534837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718d5f4b9285b19ef2b0c93ebccbee713876c8c9a3531cc4cb0ce99e66502106`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 71.7 MB (71680293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61de7971044e2680403ec5b11d13416c78430592eed6fec05fe5ce1aad8f01b4`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da61c82ee9205a9b5497541abdc5148061b3f4b2a66112508ee8979c49738b03`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3bc4f7eb65d25b1f8d920b08790b8498123055fb0f4f309ee17c9a123b36f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7231479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44f9ad559ccfa33f456e536bebc4bdc9468cddf821f57a6ef3fce609872e939`

```dockerfile
```

-	Layers:
	-	`sha256:af43a639669be7df446218275a61d1f7bc648bbb85090cf199c2f454e9601ce2`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 7.2 MB (7215834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09783154640d8a9c684d7d197b97f52fc5fbf2f6d648bdc1e8a07fe80fb69e94`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 15.6 KB (15645 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a9a7d7cbd1189a24af05724a86291bcf3c14a40401c322940460b77b42500acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267162161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d0ebcbe7233dd986b3a1381893d1f165ea225b02672fd5a4b7bb02e42e957a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cc2b2c001a978151e3adbd8857a7faf4a55640f4e035b9bea7ab040128148f`  
		Last Modified: Sat, 19 Oct 2024 12:02:26 GMT  
		Size: 144.0 MB (143959478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c17022cedcca4f23cf816ba34ca1dacb1bb37783c0f58d092c80d1b801bb9f4`  
		Last Modified: Sat, 19 Oct 2024 12:08:03 GMT  
		Size: 69.5 MB (69466747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d21457a1d2172342f8283652e739f93b4b7137a42f010f62671dd3741819cf`  
		Last Modified: Sat, 19 Oct 2024 12:08:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972c09a2931e6d7904d43e7cb3f623b33d29952d878535375226c6bedc7e4610`  
		Last Modified: Sat, 19 Oct 2024 12:08:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:241dbc3059ff796a27d2ed0fb2d8ea576a413f68e115b0e44d0596c4283feebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e65a128cd19a91d7f7df367563667fc1bce89828dc92b7938955a80064f6af`

```dockerfile
```

-	Layers:
	-	`sha256:a144d64ba4a0b825d7dc02ca4d1f090ec9e8235dc87359a0c4ac6c2f27a1edde`  
		Last Modified: Sat, 19 Oct 2024 12:08:01 GMT  
		Size: 7.2 MB (7220301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ca6bd482d9e1345109ee23bad8c465935669d1b6b4721423571deb38df7929`  
		Last Modified: Sat, 19 Oct 2024 12:08:00 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:daad1e71fa36103cfb477c6ca42b7ceeb779fb7f6d8bba5dbcead0dc609b782f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:854bcef83565abd34bda74790ef4047bcb16a479d0e30c88d10dc0848fc5be85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263905236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba87ec14f673cee1ccf0fd9d693288a3b6ce0f34784256ce002f427110df28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10374043d595d65e137c7906dac6363fb6c87450a63126c0f58d2e366449dfe`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac3f656c27fe35b45c5325d9ebf93e6aa6b969f62ced73ce49db871c95e604`  
		Last Modified: Thu, 24 Oct 2024 01:56:51 GMT  
		Size: 69.5 MB (69482770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0bf437f0660eda22ec6e1916198809602f3bc65f82fd8f13ff67f4af494eab`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e46453577d0cb01426ab5072cdb93af0add562ba3e13543e9a2e1dda3f7e15`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:be6741eb32cd193dad5614bfc35683d0ed03626aa37317082b1d9a07386b0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0211eed5a2e5067d7a1a4ed43e83145b9e24f323f0f078823d5cb84134c840d7`

```dockerfile
```

-	Layers:
	-	`sha256:b600c756fe24c9646b389ed15f8521d5d98ee298a69bc5c85fcc8a108cd1da05`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 4.9 MB (4925605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f5c02560bc42f5bc560db9248074c0f72dfd13beeb20f6b5ce1c4dfddfe3da`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 15.7 KB (15682 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbe56d215d5721414fa97ab7835228ab204f5234fad2cabbe1034d9abda8419c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261784300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65594f3895ed5e7341910f37e761c946c56c516e3a4f9b8adc5d0cba197b0511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212b9739eb7b24a5ec2f5127e76d78d0c8e76e9b3625b0f4c4ac69eb55a208a2`  
		Last Modified: Thu, 24 Oct 2024 09:37:11 GMT  
		Size: 163.3 MB (163281781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10b27125eb2a31577d0f22bcb34ab16b1d22ef29b8ff60555f180ee705be161`  
		Last Modified: Thu, 24 Oct 2024 09:43:13 GMT  
		Size: 69.3 MB (69345137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edc33e2164124cf30446fe1ecc2ef7c95fce48dd7e6af717513c8b7ff831c45`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79a55c67bdb8ac1cbd0ecbfd21848cae119582507e331f3f6ea3e5b476f61b`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b133c43d42d23a95b44e03976c9dc17bdbe80aacfd69df68cd723f13ee4a43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebad85d8a6ba9285644f495d14f6a8071e3db02ca1f2c0e202536a8d9eb290d3`

```dockerfile
```

-	Layers:
	-	`sha256:5068c6749041fb544b6ba9bf999d4ccd12c67f03fee3872fecb5a73f7e85673f`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 4.9 MB (4930749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3906a2f380b718490acdc912986d00f2d5d87d78160a8aa7668ced188b3f5c`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json

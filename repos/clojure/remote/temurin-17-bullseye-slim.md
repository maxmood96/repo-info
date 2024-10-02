## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:124bc09a1f8a3e9bbe10587fefccef144f2a12866dadd8743ae54c22267bfed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1f0fa50b724e2001e7a67bf9809bf4ea93cfc4f08b408396a4ebbbcaa198b1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235536198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9e314fcb7dc6a78fc3792e9b921b25a6c4f85c171dc876a3ec598f6043d79b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982be727563509e0718056980214de561c66b98180fac370446170fb48c18923`  
		Last Modified: Wed, 02 Oct 2024 02:57:46 GMT  
		Size: 145.2 MB (145166539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97fb093b361c386b6fd70dab6c25776da0c727e8ada67f6178308ff5764079`  
		Last Modified: Wed, 02 Oct 2024 02:57:45 GMT  
		Size: 58.9 MB (58940020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a401266bcb2e23b0ea0878b1323184d6a3b11c5920c7c1396d9bf76789ae4c2`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2489dcd91b9335f7d5167fba5f804c93645af38cb53fc30293c92b5720c7245`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5948dd495d2404ed7e628d81fa5d8e6fe218547f91d943bed5e737fee61fdc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5114363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fc4691da744c788dd4a5fa7f6b3d93d3ec72688b7e218975b040f1af8c10ad`

```dockerfile
```

-	Layers:
	-	`sha256:a8af30fc8c66bb34f58037a1f890ca27dc8261b5d04fc92844e520456e808e06`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 5.1 MB (5098845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a719f8f36cb95b20efa6a5390fd099afbccdba84d4616bf0c30e93d5c3c0ab39`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 15.5 KB (15518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d40c0ea09ac7d9ec79253cc00cb51486a21ed7e5d0fa79c7866e7182503765f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233108834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9314df4a1e8b3856e7a65d0ae25cc9489c047b9f93d3ac3db62dfc428f58f671`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a8e3a12f4cd2acc15736790a65f6dc39c26b0c97e7e637b6ec4af8c140b8b`  
		Last Modified: Wed, 02 Oct 2024 02:24:37 GMT  
		Size: 59.1 MB (59073219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f2a01a234911aabc5d150dda0723631af48d2e464ce166734eab24f1e29636`  
		Last Modified: Wed, 02 Oct 2024 02:24:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec7c6dc4da049e37428beb6d92ffc74d5192e692c2293bcffd39801a7c551c`  
		Last Modified: Wed, 02 Oct 2024 02:24:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ec92218e2b401b64cf1f6523a71b814c7c8a51a3b67075232a178a0f0c99ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fcb2bf29149b8fde71cee2ec38f45e7c56a2029e1621fdf98f655b188b8388`

```dockerfile
```

-	Layers:
	-	`sha256:6931cf66909c770889616547ffdd0995b8dc14599d10992cb181c04784b0969a`  
		Last Modified: Wed, 02 Oct 2024 02:24:35 GMT  
		Size: 5.1 MB (5104582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7405dea8247bdbee5301daf57cdc42cd1aa1baac20a2e83cfb1de7ce8712405`  
		Last Modified: Wed, 02 Oct 2024 02:24:35 GMT  
		Size: 15.6 KB (15622 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:fc6a66b6ee2010b37fc646100dc4f37b15875c578bfee2bb2e94bca17043e17e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f62049e5cb06bdca107e878ba7375cab6ad9ba43fb7cbddb644a3798605e56fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235536345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff91aa62cfea1b689254358345a83798d966477040af1ccd4b48a849cb15c2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf11a4f2a758caa6eef8194dcf705c4019176f82c2de7c1e7ac6ae426e53be7`  
		Last Modified: Wed, 16 Oct 2024 16:13:05 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182925a483d357022f1086c665a7d004996ce71b3b19b56d03cf936cd3fc7eb`  
		Last Modified: Wed, 16 Oct 2024 16:13:03 GMT  
		Size: 58.9 MB (58940141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e4c7da879aaebeb7de7bf6fa0d71d750318e36d9ff08ceda4e8c8929dc9ec1`  
		Last Modified: Wed, 16 Oct 2024 16:13:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721b215e3b8c2a3821cae93f1e66b135b91433abce7b71bec0698fbed4a96513`  
		Last Modified: Wed, 16 Oct 2024 16:13:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54791164a76cc2d482ea06a77706db7638c1fa78be9a53428b4101f9dd1c6598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5114396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c97deb1e1ce831516015e95ab776b7ec8af74e5422bd1109ec267a76c08292`

```dockerfile
```

-	Layers:
	-	`sha256:a655ce1331460cc3eee2013c03dabdcb8f8720c56e6345b10498101a3aa82dc9`  
		Last Modified: Wed, 16 Oct 2024 16:13:03 GMT  
		Size: 5.1 MB (5098845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307caf603a2212bcc06cef051cff9b8f380ecdb3d622df52a92b52cafe778afd`  
		Last Modified: Wed, 16 Oct 2024 16:13:03 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d4d465f1b3594b15602fd91f35618a92cc10daa048c350e706167e4a2f787a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233108914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297111f1571a29e0c7bfec29aae9a012dc311b81e7d6d31fe864e32f83257ac8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec42ce9ffa92f804e17aa8adf95872a1a3574976006d0237f2997f04f1c8c81`  
		Last Modified: Wed, 16 Oct 2024 02:23:59 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3710d567bb187a0ebbb61c7d40449848d40f5e4935293e6961e4db0170aa8`  
		Last Modified: Wed, 16 Oct 2024 02:30:10 GMT  
		Size: 59.1 MB (59073241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e1fee2424212bb3e07b943430134c8d025bd605799d9f91f90c0e4bae7f304`  
		Last Modified: Wed, 16 Oct 2024 02:30:09 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274c55e4719a84a699973b2e983b0db220dd3c8943a9a1ef1a63767ed5633758`  
		Last Modified: Wed, 16 Oct 2024 02:30:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c06c9ec1693d0b9f2c334c978f3a1a6451eed62d2186fa17bec8697edb628ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990bdd1acc70af81c0a1afb91f0daeea1fcd46e5272c09d9d47a68fcb54ced18`

```dockerfile
```

-	Layers:
	-	`sha256:fd4e595ca78bb873352c432f54183cc8451053904c1f9d29eec2d9e53885b8fa`  
		Last Modified: Wed, 16 Oct 2024 02:30:09 GMT  
		Size: 5.1 MB (5104582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f95c87a31fce8801ca96cadc521d35cd7cf98ef4b02f783478a1be9cff7f25`  
		Last Modified: Wed, 16 Oct 2024 02:30:09 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json

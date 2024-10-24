## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:6362cf0eed49545c46f3c33f7e9910530220ea8268c4aec33466c30552703d5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:31f493fee0684e001e01fda3363c22b1be57664adb5dbe27fc47ef6c0b4eb25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272362651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913c8693e167914a79b55129f86bbabf2a3e5e5dd61b57b2c7e865d6d6d883c5`
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
	-	`sha256:03098f0d0fd1ec2940eb820cb7d8fe1170a3b2e52c0d5bda49530b007a858f1e`  
		Last Modified: Thu, 24 Oct 2024 01:59:45 GMT  
		Size: 145.6 MB (145601283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3183262edc1bcabb8c1330fba5874dc9e8ac67a374ee7511090f6e12b2a29a8a`  
		Last Modified: Thu, 24 Oct 2024 01:59:51 GMT  
		Size: 71.7 MB (71680113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4bcf3ad11ed59dac4125b9ee1dbe4ad89feae63a7a6acd876bfefb508e9b69`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:266964d681cc0a8ee8d3cb2a768456ddf8f0d98c8b8b6be6d00df408790d3c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7250076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b422449adccf16bd65ca34d326a603ffe78c43a2823a278ead35d5c4ba08015`

```dockerfile
```

-	Layers:
	-	`sha256:15c4b1eeae0d59465d95ad75c4a82bc6e8a54a12c221e6089bd15f7e0ae103cf`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 7.2 MB (7236005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afbf6955caa4a8ebdd7f228e66c1635342e91db5cd1d2accb04b5588ae12bed5`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 14.1 KB (14071 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a9e819f7ed1e2baae6b910aa79a09208e20a61c9dde35f7520f1a6bf780cf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265557335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bac7aef78a8cf147a8748ac70559d8a64de8bfe7e1f3c2cb91bf54f722bb4c`
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
	-	`sha256:8c401c7f531d55485bd64ed4729ea50678e25946f3eaf1ab19487c5497b75ce3`  
		Last Modified: Sat, 19 Oct 2024 11:50:38 GMT  
		Size: 142.4 MB (142354834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc04cd4f9e3f29a7880732bc278005624116c146cae8a1ea0ddaf361a31f609a`  
		Last Modified: Sat, 19 Oct 2024 11:56:03 GMT  
		Size: 69.5 MB (69466962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d56a326baf54b20e3fb6727688d0dd6525bc4e039dcb947c96a9dcbbe20e520`  
		Last Modified: Sat, 19 Oct 2024 11:56:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a8f1d4845611aac0a84ef5c405980a3fec4a7121f6beded7eeac5495b25686bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7255910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f07d096f83e0e83a0dbb00a47009936461269036d45da4facc8f423bb16a438`

```dockerfile
```

-	Layers:
	-	`sha256:1c9b5089fb74699b105bde1101cc4676f38aa7311535bd99a7a2f1d5a06e4672`  
		Last Modified: Sat, 19 Oct 2024 11:56:01 GMT  
		Size: 7.2 MB (7241727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8aaf271ecc75e0dcd6d4dafe2b04d569d70f64c4c749205b3694a8e239b7327`  
		Last Modified: Sat, 19 Oct 2024 11:56:01 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json

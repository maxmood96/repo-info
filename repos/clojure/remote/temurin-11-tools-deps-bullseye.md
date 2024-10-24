## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:1e7b2d2dd87deea773d664c6ab168bb66174924f8e96ff2e1b382bc38f121090
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2a1429124223539ac38109c89d5ca0559c233f4baf8a661556fa86bda5072ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267896345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac60a210a74f8edf38409aabe1685848a07eb752f46543927870f274c3622c48`
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
	-	`sha256:4dc87e9fd068f3bebd9583290a1e1d314efdb382e2f35ea1b89944dc152a3164`  
		Last Modified: Thu, 24 Oct 2024 09:05:19 GMT  
		Size: 142.4 MB (142389121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881d5f46e725c5d03c937c30db20dd0534405068bb5ba766ca3658fb821424d5`  
		Last Modified: Thu, 24 Oct 2024 09:10:38 GMT  
		Size: 71.8 MB (71771687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1454a0f71ff9bca74c3993bbf0c4389515c5d2a31d43dc1ad81f178e70462230`  
		Last Modified: Thu, 24 Oct 2024 09:10:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5e47bb314a4ae7a05beed3bd1f1969f302bd8558b9892017396e9bd55231cd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7255909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb33fcef3f81c500a63bea67d9ac4028a4cbdb458d8a66fd3183ef8af1c2243`

```dockerfile
```

-	Layers:
	-	`sha256:a5b46e87cf166a1f36d1785035207e582638a56fbdd1ac6e046d1238a2f885f7`  
		Last Modified: Thu, 24 Oct 2024 09:10:36 GMT  
		Size: 7.2 MB (7241727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3312df5e909a56ffb38dee616cd568ee6fe5226425f357109eba9f28bb3349c`  
		Last Modified: Thu, 24 Oct 2024 09:10:35 GMT  
		Size: 14.2 KB (14182 bytes)  
		MIME: application/vnd.in-toto+json

## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b529d9fed6a74a76b80259198095d515f43affdaa0f2e9259e20eda744a70b38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a65d473dcc5c47e0365330f47b8707146803633a06584786f8e18a374df35ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e01b5f63821319fee1e30d3b7d2eb941f2b0f02679782ee348fbfcc8a289a39`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab49237006406e9b7ac3abc8904c975a5130df861c6ec73dbe2dd690ea61b34`  
		Last Modified: Sat, 12 Oct 2024 00:53:40 GMT  
		Size: 145.5 MB (145549934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaf38ee690092c4693c37bf95dbcb12c69c7b0907446a2c1fff5cfcc489d98`  
		Last Modified: Sat, 12 Oct 2024 00:53:39 GMT  
		Size: 58.9 MB (58940119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528ab99d513a5b597cacdb9bf934522b76bc1e49f0d328104500a7a3ef4ab70c`  
		Last Modified: Sat, 12 Oct 2024 00:53:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:755c24b80ffcab34c9ef20e7cbcd13130d13aa768cfc903e95df1e3708c7cdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7a746ca9464d93b071de69ea0ec6e44520426dbc2a6e50e2a827677e04c76`

```dockerfile
```

-	Layers:
	-	`sha256:f3df967d5ca243e5efb79afae4685bd20856afd6ee24ce3b86c2d7e92f62cdba`  
		Last Modified: Sat, 12 Oct 2024 00:53:38 GMT  
		Size: 5.1 MB (5119652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea9af78386fdc0e1d51d428e7330dd38b1d6a8ff5ba3037f3c3d2e3b7335d88`  
		Last Modified: Sat, 12 Oct 2024 00:53:38 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:41b9d5f4b9ec95e62f1a0be1ed3e4a1d720bce9008535760c91fd2f2b5df8284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231505738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911bf25fd4e18e42e6d53124482e85b9229675f26282b95cda986f9ac7b253a`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194c66fef25f7dc81a3ea58a1387706afcbee95076b271eb17e9ad408f2d48`  
		Last Modified: Wed, 16 Oct 2024 02:14:37 GMT  
		Size: 142.4 MB (142356565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fbf597873473a5dd2b81d56738fa629b6befd8490aafbf8a5e155de77fde9c`  
		Last Modified: Wed, 16 Oct 2024 02:19:07 GMT  
		Size: 59.1 MB (59073369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a5a2e9637c92ef049463938ea9ab4e75275af9550d5b3c7820e2d4acadac50`  
		Last Modified: Wed, 16 Oct 2024 02:19:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e43594b1b039577efeb77293120b57a2cfa8d7236f3e3c626106cff83836ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad91fac1ab1879b1878aea50e7928c53e71f7b9e45ed856827296959e99c54`

```dockerfile
```

-	Layers:
	-	`sha256:f74d7d919bb986fe0cbedd6913e0b907974314bba1567c710c696c5c23fa80c9`  
		Last Modified: Wed, 16 Oct 2024 02:19:06 GMT  
		Size: 5.1 MB (5126008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7412a363571deee255ce6f3fd33dbfaca5a318fae7cbef47c15f9ca49446c8f2`  
		Last Modified: Wed, 16 Oct 2024 02:19:05 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json

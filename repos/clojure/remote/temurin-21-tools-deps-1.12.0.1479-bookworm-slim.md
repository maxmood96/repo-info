## `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:ffb1749ec37deee0fc002187cddd1a0daf89bcbb6376ac8433cb204e5a8d231e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9fdfec8926d387b50f2c08a2d2b59d8514c785fe45d99a986e318e69c85ffedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257189009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ca79ac966c5d654a69c19304b6ba5b9fe84d9a88defe41242d689558af3841`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e3920ef71fff1f59719fb0689e5d52531eeef7e6f6d7101ae7e161c2be8e2`  
		Last Modified: Sat, 12 Oct 2024 00:54:03 GMT  
		Size: 158.6 MB (158579253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a632d843c5c0d84202ba4cbaff8b82d5a8833a1d80e891a4f460f40c74bf948`  
		Last Modified: Sat, 12 Oct 2024 00:54:02 GMT  
		Size: 69.5 MB (69482437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8859a22953579c7bba45756ee3aa36a4d1b74511a92ce4ae34fbcb57f983c2`  
		Last Modified: Sat, 12 Oct 2024 00:54:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048f902e2f0f96c1add4a80f73fb906efb05a848173d11aaa4857287e25e7996`  
		Last Modified: Sat, 12 Oct 2024 00:54:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6cd0f1a94dd3455c54d760b117874f17ca3a879091a3970194cb9e8ce1f1f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0f6d3d473dc0c578217b07a2ecd6d3b0bad230b418112d55dca3bdb6a1a51d`

```dockerfile
```

-	Layers:
	-	`sha256:30c6fee056df4232e4db373dd6b40486f14fe794e253edffa8ca42b1c7173c1a`  
		Last Modified: Sat, 12 Oct 2024 00:54:02 GMT  
		Size: 4.9 MB (4898648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e62cb258a7da9c3cd44e0b070ff829e868119bc2ea5001f6a6484a370a953e6`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 16.2 KB (16211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d5a5c34c42490a3b4b8250d06659468950dba2ac30b0a837457ad2c07794438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255248834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20aa6549d10582616285c64339ad6cc193ce29ceffc96dd744059b3819c4e30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589611fafd772edac0bca816cacb89a5847853abfd91c2eaab4e3b021c481ac3`  
		Last Modified: Sat, 12 Oct 2024 01:22:56 GMT  
		Size: 156.7 MB (156746170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42c80735b01653597fc320fa5e79881f0f4739d2bc91559f34315057f628ae`  
		Last Modified: Sat, 12 Oct 2024 01:28:13 GMT  
		Size: 69.3 MB (69345256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a967b13aad880a23b14d0ce92f10ce1873939432dfc297d8358aaed8d9de881a`  
		Last Modified: Sat, 12 Oct 2024 01:28:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43681158d1060ef61b4641d493dec521109bed1d244442cd0a4e9af3d3cc7b4a`  
		Last Modified: Sat, 12 Oct 2024 01:28:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6dc9b46dca02d1b8ead0d541310ed8fa038c35d0648d6e7ae7687182afe730f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7022d72adfbc9a646db2c932f99c0dafdd1574af30efce0952561f973d9bd70`

```dockerfile
```

-	Layers:
	-	`sha256:d8459a83f05f363109031b87dec3e6ce3d2929e1602a680faf164a3b69dd68ea`  
		Last Modified: Sat, 12 Oct 2024 01:28:11 GMT  
		Size: 4.9 MB (4904438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8202561c8dd1db4ce7eca0eb3567414f667b4feed97965cb8eb030c83535b66`  
		Last Modified: Sat, 12 Oct 2024 01:28:11 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

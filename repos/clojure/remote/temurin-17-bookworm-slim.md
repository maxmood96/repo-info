## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:ebce9bdb0330e3301b532afaf405488694ae1bf84b0ca2702f357dbe2b7636e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b13df6c0981f755b070f0049076a4fc989361537f6447a453c8f061001089022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d65ccdf066763fdd5dd571965f94550d634f1f241feca2cbe42bc80b857936`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095f8a545bef697e105e67c2d9706822fdc397383573ca660b3e95fbce34385`  
		Last Modified: Fri, 27 Sep 2024 06:01:16 GMT  
		Size: 145.2 MB (145166557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2768cb41e5c36ff84d6fb38fdacadbe4299ad290a2e971894d4acb812aeeddb7`  
		Last Modified: Fri, 27 Sep 2024 06:01:15 GMT  
		Size: 69.5 MB (69482776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11083af72f66c456896372c48766224a6dfc23ac76353d80359ba87e5d22c1cc`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464cbdad27bdc4bd3e7efe093254de8d76f1c23b095f2ffd0117d4698436c24`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8cc810d8d8adc367459db7dacde5212316061eeed06a6b95a47f29e9eb44773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4909723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa39146dbf3d60db71e014a0a9e86f332be65e8c648185852dca79b762953c2f`

```dockerfile
```

-	Layers:
	-	`sha256:801b751a6a12c9172b17b2e59d50b34c8214e28795de1f3fe1d3b89c5288235c`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 4.9 MB (4894211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175b1d2d93a455b7932f9e4d4a0fd939107247e7e90117bfe946ffe2c723e280`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:64fa886124b3e33228ae931b545aa38e3688008b29b029d581f0c49b3ca62c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242462302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac7f0819035342fdef1a5cbd35517e222a5140c3102eb29f6ccf43a3ee2faf6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740cd234f8bf528b6fefe9b611e99c48f93c234f58c315a5d6fe64e533ab84ca`  
		Last Modified: Fri, 27 Sep 2024 10:33:02 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325c37344b4f212b0cbf5e86ae43c58a34e20dba5b907ad50c26cbbfbfe3cb44`  
		Last Modified: Fri, 27 Sep 2024 10:36:52 GMT  
		Size: 69.3 MB (69345427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6327fbc02bd5812e01beb2615c8d8a3c2a90e7eb2600ad04497bb8c1bf6c3524`  
		Last Modified: Fri, 27 Sep 2024 10:36:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c988bce11ec073fe767df4861519959798abfc0b0b04aeb09488c6a821da4778`  
		Last Modified: Fri, 27 Sep 2024 10:36:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e23d904fc28e2842f8b6cf9f39774bf5993e4e54dd1f03712ce5ab873b0402c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4916030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9e45493c199f5bd6a3e547ccfb2d391fb37bed9673a949228a90cff423faa`

```dockerfile
```

-	Layers:
	-	`sha256:2da55de89ce4f7eafa50f7599ebe2ca389fd6e9a594e8dfb041f6338c8c573de`  
		Last Modified: Fri, 27 Sep 2024 10:36:50 GMT  
		Size: 4.9 MB (4899977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a51942b3177e1b9e61e64dd1cfbef1b1d9383f931cafc1a151e6915ecee0ab1`  
		Last Modified: Fri, 27 Sep 2024 10:36:50 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json

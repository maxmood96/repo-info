## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:dd3fea7c1d9aadc1c93049915a16070e247555e5b8cb807d599592d3c0b824fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ea29e09e571cf87e2caf74c111dc2eacbe9bdaad2e46ff25afdf6d5ba07e6c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257189227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f06ca261f6ee1b0ce70121f448c89b601835f0f798f72d8346ab3d460a6f1a`
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
	-	`sha256:51a81c4ac3e60ac42a5cb2fb34af019893c4701dd59aced4b032fdf6b7ac8714`  
		Last Modified: Wed, 16 Oct 2024 16:13:20 GMT  
		Size: 158.6 MB (158579255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d763ad93839eff780b14dae62db45c785a825281a513d9889b6d43478db3731d`  
		Last Modified: Wed, 16 Oct 2024 16:13:19 GMT  
		Size: 69.5 MB (69482651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defaae915667d9906d5b2c3d72bf79175951313cdb3ab08757d85a4bc7340146`  
		Last Modified: Wed, 16 Oct 2024 16:13:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a34fcf505ab004df1cdb7723003b6ec0fa79029d4358142ad1216bf17e3bf`  
		Last Modified: Wed, 16 Oct 2024 16:13:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c6c4146eddc45c6546dbbe027c4b561b2a6605afde69e0e93a5fc9715245a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a21e42c2df273f2a11fd87f0e61395c869ef1d55abd86f7c33b6bacca627b59`

```dockerfile
```

-	Layers:
	-	`sha256:7742f5934b7779d2c0ab7e77b0c8eb675a6da19ce247a99bd3d9024e49016b59`  
		Last Modified: Wed, 16 Oct 2024 16:13:18 GMT  
		Size: 4.9 MB (4898648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccd33883edba06a026d32b0b7ef1daf17afcfce6e2e2eef19af2d247a4b45fa`  
		Last Modified: Wed, 16 Oct 2024 16:13:17 GMT  
		Size: 16.2 KB (16211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:098b4bb58fc89cc3e8292a60211a9c866acc661bd3b05b054348f85d3c39ccde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d037e62f8bccb910a01b4b4818e57dc6a7e2a35608a8afec748338b4f3368fe`

```dockerfile
```

-	Layers:
	-	`sha256:04f184c88e73b189e7f7965608b375d9a218b0c6a550b49d9c62ee5cd1003073`  
		Last Modified: Wed, 16 Oct 2024 02:35:51 GMT  
		Size: 4.9 MB (4904438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b03e71b72ba22f80d284d5cea0a265740e63614017ddef9e45736ab4ab7c6df`  
		Last Modified: Wed, 16 Oct 2024 02:35:51 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

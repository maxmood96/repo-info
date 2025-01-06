## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:cdc88310bb16dba4f8adac18a65642f86f6d050452e827f5222e7266c70e672e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:646fc933d84c047a1f2b98aba9f72b6f57bb12dd9427aba8f74677b388529126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294537441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78e80d0383d209a4e811a80d8cd523d384c9b1a4eff95517d2792d40984b73a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d760ac17e45d3321880494fc84d74adc4e770c4f5a24b2843c41f16eaf54d91`  
		Last Modified: Tue, 24 Dec 2024 22:38:45 GMT  
		Size: 165.3 MB (165295092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2548782c7de41cb65099b0b180d162799d354bfff070b8dcb9fc2bb638a05`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 80.7 MB (80744244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b68d62bec92e4765b2f93f117374d9d96b702ed69bda32ea4e833b0f3ef764`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc339761a3234fa28c37fdcf3acbf0f5dcbce5b9fbb4c174438bde9c8ef6e002`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f3ce9522fc4bb8cba6aab290925bc154449a9f24ace5a93014d9bb7841a0560d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0018e7a3818aed31f5a6d7fa526f7bc8bc9fbf460fe2a15c8330761053183037`

```dockerfile
```

-	Layers:
	-	`sha256:11b3bc0f9c9df9f1eefddc20ad1cb05d96cb00225e0dd3a8bfe605532ddf4d47`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 7.2 MB (7176707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e48ef6cbdb84671e1d1cb1cd4637b69a5997ab2eb112398969330d94154f55`  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:505b3b6f8c99fb462d8d425cbdb8889e6c9b3e6cca56d454bcf16ae5354cd12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292213861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a30300831691c2b924c835ee889efefaf941866cd92853e45f9e75b411b31e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05182ce04270e6342718b72641c3eaee0e4fc79c31cbffebd00bee2cdf25c2e6`  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf21bbead96b90384b568c336e11fab3de22ba057da778641556e5da9ea5844`  
		Last Modified: Wed, 25 Dec 2024 07:40:40 GMT  
		Size: 80.6 MB (80605544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef1bbaa590055944af365a0b3dab2bc0844bc135491105c9deaff44ec46f6a`  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b929a96cc46769aa166d6911a97de14bdc027b83ad99f9f4bea32a99220a41e`  
		Last Modified: Wed, 25 Dec 2024 07:40:38 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2fb257e771b4709c41f47da2602bbe4d72881f5b470aeab5a4664f898da45f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9656103d5476fa481fa5b9d7c0082ef137a3346615f16a9134fd3f8007ca8d`

```dockerfile
```

-	Layers:
	-	`sha256:988ce4aa2812709bea25d01e62417b25ea22ffb6ad07863594e57dfb45034875`  
		Last Modified: Wed, 25 Dec 2024 07:40:39 GMT  
		Size: 7.2 MB (7181873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33530bdecab6449b932d99e95156517b27dcc514423267aa68180af7675978c`  
		Last Modified: Wed, 25 Dec 2024 07:40:38 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

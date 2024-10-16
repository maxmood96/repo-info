## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:17c07491792b5bd617c03cb59d66d691a9aa29c35c65059300e32acd517d0c32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:76bf4e32d2d40d9fdf09d71c44c4a19aac113b033c5a882ddbaa7bbcf0cde594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263877772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea95dc970ecf66df6dbce8d557cf42e9d7217605c2628e7ce84466aac67d5502`
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
	-	`sha256:1ada267bf5ac114f84ed720f1564b96662e12bff6e4611e2e110dea3778b157a`  
		Last Modified: Wed, 16 Oct 2024 16:14:47 GMT  
		Size: 165.3 MB (165267599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304f2402a78c426b88a40aae7545b1bef55c4a449c26d2a78cc11483289edc5`  
		Last Modified: Wed, 16 Oct 2024 16:14:45 GMT  
		Size: 69.5 MB (69482855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6aff9ad5a27956e31b0f81bd17f065a3939114992cc6d30238f6320982ed23`  
		Last Modified: Wed, 16 Oct 2024 16:14:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f28b7c274a3452d20990084611d51f6a292bb35f21e5c4f3d0816bafbe9c352`  
		Last Modified: Wed, 16 Oct 2024 16:14:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a35081628eec890d70f3a4486962b1d98aa401e417603433e8aa2e5413cfab85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b70650cecf12c51aec7649b8fd070be6845f11831bba6ea980a792ceff8a87`

```dockerfile
```

-	Layers:
	-	`sha256:dadddac275ae1d4ecb511daf08c8d5e579ef96640cf9b48db3ea244ff75f53e0`  
		Last Modified: Wed, 16 Oct 2024 16:14:43 GMT  
		Size: 4.9 MB (4899844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:205b0c1bf97ec6efb33d97c3bd0844c0746fcec9f788eea57b10f858aad30044`  
		Last Modified: Wed, 16 Oct 2024 16:14:42 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5725a9732abd0aad67b9109b7b1292f453e9b6d7bfd20a98bce39ceb2a9727f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261755577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb918d864dfa89d950bdbea3e86d360765af7f110b7d2dd02f741f54a2a56fd9`
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
	-	`sha256:851cc9fb21ca2ac3e3b1cefe22c283c974831b271df8829329a5ef738df50261`  
		Last Modified: Sat, 12 Oct 2024 01:33:12 GMT  
		Size: 163.3 MB (163252850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776dc9f90a57090783636b142c511ededfcd0e6370864f2165cef8145496049e`  
		Last Modified: Sat, 12 Oct 2024 01:37:48 GMT  
		Size: 69.3 MB (69345317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c53cb91a1e82c44bd65aa003137fd75b357c1742beb7bddc1ff716fef715e`  
		Last Modified: Sat, 12 Oct 2024 01:37:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea752e380c96041f3a6dbc234d8c93ff2cd97acb5bfb496910c1e933410364e4`  
		Last Modified: Sat, 12 Oct 2024 01:37:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65063e368b07fc979c03b059040fc05df6b8a42ecbffa5bd9d913310bbd2a162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbf2249e714d51b02d70a417978736a182568254ad4de9c0ff395253212ce9e`

```dockerfile
```

-	Layers:
	-	`sha256:db0a4fc784ac1c540c9f074985815d31015ad42e38c24b3a7c4d77ec0f4b31a7`  
		Last Modified: Wed, 16 Oct 2024 02:42:16 GMT  
		Size: 4.9 MB (4904988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d89bc625e1cf3c7b19b587de5819f847146d39c1eaa59427f2fd025718a1f2d`  
		Last Modified: Wed, 16 Oct 2024 02:42:16 GMT  
		Size: 15.7 KB (15656 bytes)  
		MIME: application/vnd.in-toto+json

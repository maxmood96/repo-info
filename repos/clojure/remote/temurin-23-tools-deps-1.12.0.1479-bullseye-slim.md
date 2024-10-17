## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:db99e7ff053509ddacba1c35e3e49a608047ad6faac53fdf05b78c87a5929b5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61d5740d35f870df400e3f8c04461e08b2cd336629e45a1a07310eeee5a1a9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255637534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3011d64fb13b1214312089283ccef9577205984f77c7584557e2d2d6a7e98985`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68f122a48350ce95e50896724eca961fdb8235429755ef94bb4ebd2a551d57e`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 165.3 MB (165267630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e582d30e4670db098db58dda31b585e5f44753103fde048b69551a1b5517169a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 58.9 MB (58940065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94580c18e453d533a6df4758784eaa7be5cd32876b4556b30ba4d2e1555c4779`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7475e678dd4a576d64a8f1ab5c4dba1c5510825e941722fa37fadf62b6d7b`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e61e48bb5a450813f808383b90d4232c25341bca30c3e04923229f203e07cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1ea58f0101828d423477edff53ec3427ac87b42850159d6ddf0b81bab19fb1`

```dockerfile
```

-	Layers:
	-	`sha256:a6b05eec74ab42f3758fd7247c41f1f1c41a36433ec4920738f08ec12b1ef63a`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 5.1 MB (5104568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd7950811bb9be0a966a360055b2c761fb9ddb73ea14d9b95d03bd00ffd41be`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77a16df50a67d8d4b93f2ad0f41f9fee6e7360cad9e09bcb9fe594ccb897bb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252402667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4885cbc3aff22cc44802302235818a398896afa4d6e02af898151ae7d52e4dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef34680c3ee0cb00936471ae2c979a3b313bd7bb6fd8b2e8a4124061a483fef`  
		Last Modified: Thu, 17 Oct 2024 08:31:05 GMT  
		Size: 163.3 MB (163252839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e646fc2ccb4d95c746d3377c4bc568fd7558f45aca47d22a9d4c8414ddf80027`  
		Last Modified: Thu, 17 Oct 2024 08:34:59 GMT  
		Size: 59.1 MB (59073032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613fe3b7e759b31ff574545b3cc9f38d75f65ac367f819077a9c47e2f99ed3c`  
		Last Modified: Thu, 17 Oct 2024 08:34:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6e9245f855940fbcd92121e2b6fcee7011588030c3107586bc3f4ac2a5e0ed`  
		Last Modified: Thu, 17 Oct 2024 08:34:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a7cb054fbf0b86d6240a6203b97a7b8a004f37fbe57693e950428258924c623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ad7990ddb993f43f2b8edda0d821d90b6b9bd8549af705ec4ce27d88dd12c3`

```dockerfile
```

-	Layers:
	-	`sha256:e8d747fd922eee9d325745d18e1a7f386f1834d99b547bc62ca83ec16c050462`  
		Last Modified: Thu, 17 Oct 2024 08:34:58 GMT  
		Size: 5.1 MB (5109683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22171e57466f2da006d841d48230a4dfc5b1ab93193a829e0a040cde33d1634`  
		Last Modified: Thu, 17 Oct 2024 08:34:58 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json

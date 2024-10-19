## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:f22d9c0320f619a5914801b1b402140ba00d543048f8b0dce8de971166d649f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ca25a188662de8227a51f9b50515ca165f8a2e763c4c043cc8125d90b825de2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275650834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64355e191b5382e60a8ac519c9bf91ab564bb834f49d15ef8e2ce1cdf397bef1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33d1c4516450ffd846b3db3ef64661d7189a8b9e18193197402485c8d9db58b`  
		Last Modified: Sat, 19 Oct 2024 02:55:51 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e0ac46e3d87e938d3b9d0deba62f16d4084ea2f894f001d6dcbac174956d77`  
		Last Modified: Sat, 19 Oct 2024 02:55:50 GMT  
		Size: 80.9 MB (80928234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb0acbf6a1664b22c9624658be08c5816a88f08ef36fa853d374286a1e6cbd1`  
		Last Modified: Sat, 19 Oct 2024 02:55:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4455d4ef7e544668f8029a14b95c0f05bafaaf84a56477bd8f179b08ba9722a`  
		Last Modified: Sat, 19 Oct 2024 02:55:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8aa0b4e811ceb5994e36f3ed316f396b886fe50089756f4843e52b068947e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb872adfbbf02194f5835b4f467d84ce36fb1731194f96c601ea036a7193148`

```dockerfile
```

-	Layers:
	-	`sha256:b4ea9e4a1152af8ffb9c92e00aebd89c0a94401a84d14d5cd12d8bdc441114d9`  
		Last Modified: Sat, 19 Oct 2024 02:55:48 GMT  
		Size: 7.2 MB (7181751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2e92155e162ee76486aaed884283d966710b9a6623b2dc51d5a36cbf2dc025`  
		Last Modified: Sat, 19 Oct 2024 02:55:47 GMT  
		Size: 15.6 KB (15646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:320bf0f1c96f0558dad596e0cc903f93c984bb4ab16583589889045a93735d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274335545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3271405a1bdf6c78265d374b6e50fafdd48c4b2b271b0762db28d260df5c4587`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af79cbd2bebb502c38437b7b81f3b9697a59e5f45be49cd74b73bdf63f10ac08`  
		Last Modified: Thu, 17 Oct 2024 08:11:33 GMT  
		Size: 144.0 MB (143959476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8e70c0e27f916331f49a283267e3e257bbdf87e572c6f36ce5027dad023c85`  
		Last Modified: Thu, 17 Oct 2024 08:15:51 GMT  
		Size: 80.8 MB (80790050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f670afbf9852f5caceb4280e54536843c50f984fe64afd5e4f5dc1bff5ab2`  
		Last Modified: Thu, 17 Oct 2024 08:15:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc01a5b0dc85d191e594ef288946e0cde25e66fadaa921e675ebbb4c939e6dc`  
		Last Modified: Thu, 17 Oct 2024 08:15:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9bdae866eae3728f33ab5557871366e3209df9edc39486c02ba4e6f7892abceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7177357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb84bda3159213a82c8a544fc3b2371dbe29dd355b1ddcf35cf8e9759214f43`

```dockerfile
```

-	Layers:
	-	`sha256:c3cf51aef7296fb3b4bc39e303a252ec86f17fdfe890a065e8c2e173a9aa287f`  
		Last Modified: Thu, 17 Oct 2024 08:15:50 GMT  
		Size: 7.2 MB (7161774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0003de83cdb8d2ad0e8680f26595217fdf942e8bdd548a25a805bb72f3c7d25`  
		Last Modified: Thu, 17 Oct 2024 08:15:49 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

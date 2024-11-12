## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:54f2d2409a6c334ddeadf042d80e7c2348070bc9e99cf2f0a025f8625a57a8cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:086feffd7511df430538db51953f3b1aa97d993c6f354ddb47b30a28268c72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75897933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153f69c84916f02f4a6dc6dea4288fbd5e0f117dbb28cc409a6c83d94b148960`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885590f1f7b0d800a74c7fafd930c3af61b5fe15daab2678bce790c7f2f9cd22`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac53a171ae4ce01f5e27baec3ad5f6f037a1881b346195983a643819a07b883`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 292.6 KB (292605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888177041de4c96b1f68418e7bc5cd4687108fbcbc610cfc109e1ed4b0bda3c6`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 72.0 MB (71980643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f14c58286ce05ab80eb37c85d56c1be46dad43efe846b230ab9485fd49396`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d341b2a713279282b63733cc3f66bea88f5d3f1a02213be85948833f8061d`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:fd6657b7e90030fbb5a9534bffa32859cd913c81d638b9d597a0b4e53d93817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0bdcc14d39feff37d8496fd2d25c12af54310733fcb8271d15baa6b2dc768b`

```dockerfile
```

-	Layers:
	-	`sha256:cba342c70ae180705b80a828265e8fa05932dee56ee3dcf1ec209aada94ec9d8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 365.1 KB (365112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6097a085c6c0682ab3aec996dd441ead4d2d4f3eafed141ab953b589e3b790f2`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

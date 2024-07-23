## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:bda6f3cb67284c0da5c9011100201d870ac597821831c340fc1dfc0d314766a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2901c06ba0aa8e1ca321512279411eae4fcc4cd07d1cdd2c9381c46fd51de58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31806919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1e35742a524fbb3a01981ea10844eb8ae62ef954762a43772bcb695a2f9d68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558a15ffd5fd7dc1a320904adf4538b87b67a939d5d006b98a9b36017947502`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da05f34e03c0428cf96e2e8e8754fecd048b4672e1675c8dfd091987120152`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 292.6 KB (292596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f4131f7e5257e9bc0a1099c0b2f6bced312d6e6f67a5aacc49361fc2c644`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 27.9 MB (27866731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe17f4dd5d6655838dc7645cfdc88d3d95367154f129fe3d96acac7ee78a03`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c01279850cada9d2f470c39fdb304fc4ce71db414de5c5711c4bf17239418f`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacddbfa4fec719daff43f784bec28523cd8ee4fcc4786ce979c93515cadf4ed`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6529e5937f5575e4cfb5f64c28d37ad905a0661f7072532e29e5ad2854533e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ed52c6d0f8dbb2cbd26f76933a42d8893154547aa43e6e3b1189777362aae3`

```dockerfile
```

-	Layers:
	-	`sha256:2b633ff9323f7d9bf699a774058c48c851bf8eca1471aba989ded877d8c6b88d`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 239.6 KB (239587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c025800fabbad37f8d0a4823f2cd8491208afe5abbb959cf08ed7afa251e434`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

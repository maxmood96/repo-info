## `aerospike:latest`

```console
$ docker pull aerospike@sha256:a35d8cdbfeb40ffe06c3961ebe21484020a1296bcfc625f46eacdb574a3ad914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:1558f2cb3ca662550ec9acd2ad059b9a4b0f21adf916c42d5cef9067e5cc1706
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4601bc7fc4b11a0f9e95646b8c2c15290635b8ffaa812703aa314505c719599`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 13 May 2020 21:23:54 GMT
ADD file:3e0b81347262efc5a7401a531be7ab45cb8ab05ddab528fbb849bea0053865a0 in / 
# Wed, 13 May 2020 21:23:54 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:48:09 GMT
ENV AEROSPIKE_VERSION=4.9.0.5
# Wed, 13 May 2020 21:48:09 GMT
ENV AEROSPIKE_SHA256=7e9b345020e987d1a4d1c91034a8054c97fd80a0c917a8da04d4aad9127e8fe2
# Wed, 13 May 2020 21:48:28 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 13 May 2020 21:48:28 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 13 May 2020 21:48:28 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 13 May 2020 21:48:28 GMT
VOLUME [/opt/aerospike/data]
# Wed, 13 May 2020 21:48:29 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 13 May 2020 21:48:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2020 21:48:29 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e4f2068f62324fe92e80c472afb3742bf506f2a52712bf36ec0456de94c5b14e`  
		Last Modified: Wed, 13 May 2020 21:30:12 GMT  
		Size: 22.5 MB (22513438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e2664c72d3ddcd888ea3d3f238d87c0c4ab925c579f6edb176fc3df7e4ab52`  
		Last Modified: Wed, 13 May 2020 21:49:02 GMT  
		Size: 30.7 MB (30670535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e743efae275c5ab33e4128bf3e1b07062117d666f75780357ebc27931b58e1f`  
		Last Modified: Wed, 13 May 2020 21:48:56 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae1d6596fb0d8eba9e5a01b5f5fb107e82f1d299bb40dfbda73a5ad8b4e9f47`  
		Last Modified: Wed, 13 May 2020 21:48:56 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

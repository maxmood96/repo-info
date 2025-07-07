## `openjdk:25-ea-30-jdk`

```console
$ docker pull openjdk@sha256:07853fa0f5ef0fc5e3bf31aefe151b138f3a1a9e80b12b78d402530fb9b4dedb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-30-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a5cb5d4a7921f573675d6374b574dd79154241007d8776f5928ede0b8814c03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310648292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d5d5bf5353325e38e7d4fd2e7e9e045a320ece62fbcbe1591363b9862a2455`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jul 2025 18:39:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:39:37 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad0cab3faec3438bcfbccacca666f745132fdfb9c0b58be7d741f94c36a176`  
		Last Modified: Mon, 07 Jul 2025 21:00:12 GMT  
		Size: 38.1 MB (38092469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9147bc517b3cefdb78a99efe0f50b2427dc09f0c0dc058dfd1bb7b1d57784a5d`  
		Last Modified: Mon, 07 Jul 2025 21:34:12 GMT  
		Size: 223.1 MB (223055275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-30-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:75b8173946f66cda1e6e5e0266834559e8de96d6c01c648cfcc973e15bf1b983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b888151f5447c053f82e530efa4e371b076f58c802a943b2f19ec2b35a12d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cb57cc7296acb5638fdae42235171dc086cee2dec01aababa23d18ba6fd5fae1`  
		Last Modified: Mon, 07 Jul 2025 21:23:21 GMT  
		Size: 3.6 MB (3641308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a11356e5b6eff60e7136a3053b3000c501697e0448cec4a0c680469914a276f`  
		Last Modified: Mon, 07 Jul 2025 21:23:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-30-jdk` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:b465a4175b4d5107f23fe193b13b3e54b12fe3cc34d7eca74dc6ee7074247b01
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499862580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae92283a71c98b78928e6d79e99b9bf26130dad670c448cb35271ed94e59301`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 07 Jul 2025 20:59:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 20:59:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 20:59:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:34 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 20:59:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_windows-x64_bin.zip
# Mon, 07 Jul 2025 20:59:36 GMT
ENV JAVA_SHA256=917fc8ab9ae5f7aa7aa1d45bd5a8612a2fd33d6835b9a42728532d0a14f8b42e
# Mon, 07 Jul 2025 20:59:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:00:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f18c600e3f1e6920a9c13e2bc1cb85fe722ed3f4c485d7232ab8b219784bdb`  
		Last Modified: Mon, 07 Jul 2025 21:00:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eceaeca1107bb95fdc4e4cf9e11b6ab194048ffc8d2dcbac5d04a78f093cce5`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 356.7 KB (356728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff3c45c8aa311b9ea73d06c6812e68a19df67ef9b9620162bb77958a8cde4`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d2c54236a297b70de340f1058bf553e9f801f477c9bf5f3f3a781810e731c`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 345.4 KB (345449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea667565e692cf293be7cb956420752cfa282d797157fe71009c15e4c6afcea`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0844edca565cc66cea58c88d52881bcf4ec81bf0d8597e8725497acf387b6a69`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6426423c9c77930251dba727e82e1616b45f18e4dc07733653607065b30874`  
		Last Modified: Mon, 07 Jul 2025 21:00:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4142f979958b0d74dacddbf46f937781885770bc9abbf4116b435e3b72b25531`  
		Last Modified: Mon, 07 Jul 2025 21:05:52 GMT  
		Size: 218.9 MB (218901116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325bc6bc2c5ff81b9dab75b85fcea93ffe06f03ccec9027af8b78444a00a305d`  
		Last Modified: Mon, 07 Jul 2025 21:00:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

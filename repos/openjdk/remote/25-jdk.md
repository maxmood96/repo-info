## `openjdk:25-jdk`

```console
$ docker pull openjdk@sha256:187300b3d839ac8efb2bcc714f2bbf85c71731ff0e274a0df24657c3d14f5b09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7c61a77efcda275a3884cc7b4a3cdbdc0af56bdf531167be970d9b3d899ba0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310560377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c685aa29d4361533a9408156d721351ff9908990e728ab8155259bd05842f31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 06:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55da7740d2fc1993092582883380bd30f04279370067363e4920f684c4603c4`  
		Last Modified: Wed, 11 Jun 2025 17:33:44 GMT  
		Size: 38.1 MB (38081375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c87f4af59a1769a173b3061f069d6a7c3e1a0c1bbe082ad924db3e0a53e437`  
		Last Modified: Wed, 11 Jun 2025 18:25:01 GMT  
		Size: 223.0 MB (222978105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:95d6e55a7a96d783271bd88de43f22aebf62bb37616a2d405063769009cfaebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139184294d550cae41c20ca84262cee3f857f4f15224b70a7e4d0886cf14148b`

```dockerfile
```

-	Layers:
	-	`sha256:6a80b3172083238b584ebcdd2679f29d5e0ca6d75c5d94bf25ef56402d076d5a`  
		Last Modified: Wed, 11 Jun 2025 18:23:19 GMT  
		Size: 3.6 MB (3641236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc318ebc1584df833e373c79d8aba00bae79e2d49e7ba4fb8a9c160481cef0e7`  
		Last Modified: Wed, 11 Jun 2025 18:23:20 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5fc02520792e6ef05ac16d9f5bdbd31f5852dbfbd288ec33b77b15b8b05bdd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307355571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2fb726af5b83fe7f4e356adbc82e6d8339f64dc22c4fcf995db2db27bd9c2f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:25:38 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:25:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cfd988351345b9f04447fdf8c2c46e73b5a5a2afdfe346ff0026d0c170ac82`  
		Last Modified: Tue, 03 Jun 2025 13:49:29 GMT  
		Size: 38.5 MB (38495973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b5aa78add0916ace39c3afa9cf14b69ebc9e6f691b5df9d5dfb3ed1c4c96ec`  
		Last Modified: Tue, 10 Jun 2025 01:51:22 GMT  
		Size: 220.8 MB (220769019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f6c257f44d721e62cd6214b0f04b22e438af8f06960c8e833442bee2c49bd6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9315bf9ddcb5a96017890fea7fd7a4299cfb9b4f3bf9a38264c9941a7373d520`

```dockerfile
```

-	Layers:
	-	`sha256:7926f16f05de0ae2987b10996586cb5a9efc7a9023bf37ab07ba67011feeb519`  
		Last Modified: Tue, 10 Jun 2025 00:23:32 GMT  
		Size: 3.6 MB (3638998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e28e7299dd798acd06c9e6d0206568c7715ccc1e8ebc251d8c869c1a1f7340c`  
		Last Modified: Tue, 10 Jun 2025 00:23:33 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:c32983bf6784a308aea6cc8b612006e1bcb5b1b1686ea845896c69c018cd3927
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695802801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d306593e71c40f5af2cbc3526c62e63bc77702d26c9d174d3aaba8872f5c2ce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:27:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:28:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:28:06 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Jun 2025 21:28:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:28:13 GMT
ENV JAVA_VERSION=25-ea+26
# Tue, 10 Jun 2025 21:28:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_windows-x64_bin.zip
# Tue, 10 Jun 2025 21:28:15 GMT
ENV JAVA_SHA256=6600725ff08e343ea49db5bdac0cc8ef756053c899efb6a504b5f9e4a2fcc69d
# Tue, 10 Jun 2025 21:28:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:28:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef4b57e50361d525cff5f7b93e36265c02dfa0d8fee3ee03f5792cd65fb50fd`  
		Last Modified: Tue, 10 Jun 2025 22:09:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4be9fa038c4acf1e421dbdd91c9476e452c656278ba7ef25ac939085fd1eed`  
		Last Modified: Tue, 10 Jun 2025 22:09:47 GMT  
		Size: 389.2 KB (389218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3e59d2e84aea41657254e4b258cbcbddc2c72f683c6bc75401eafb041295f8`  
		Last Modified: Tue, 10 Jun 2025 22:09:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d67d6f694a2cebd0a8c124056890845a0922b09eb18fa5da8b829208e1316fd`  
		Last Modified: Tue, 10 Jun 2025 22:09:48 GMT  
		Size: 377.2 KB (377250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1b3e332dd121f8f8956360ef9a52169a075709c9884e10a6ce5438aac7833f`  
		Last Modified: Tue, 10 Jun 2025 22:09:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192fb2d10d690b9ab11e9144ef0f1bfef018bbbac929ba71a12c6823df062ec`  
		Last Modified: Tue, 10 Jun 2025 22:09:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81d7932f218ea04cde48704cade926c5dc52929766d90a52afa4af18e1c640e`  
		Last Modified: Tue, 10 Jun 2025 22:09:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1344744fc3e9e6a8fa0cb13d326831b5b1283ad8f516cdfb21dc67bf0a90c594`  
		Last Modified: Tue, 10 Jun 2025 22:10:01 GMT  
		Size: 218.9 MB (218854534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb07467490a3b1b892d6f1d8a7b60a71a28e005104fca3c136c54752b029802`  
		Last Modified: Tue, 10 Jun 2025 22:10:11 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:8a213e29edd9fe8194b7e2dda3b643ab9f992fa6168d11a95d6514892fea028e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499742573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5572229b1bca8f9827b0d566f2de185bd571ab30bc40c647abb414ba8cf16fa3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:35:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:35:24 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Jun 2025 21:35:29 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:35:30 GMT
ENV JAVA_VERSION=25-ea+26
# Tue, 10 Jun 2025 21:35:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_windows-x64_bin.zip
# Tue, 10 Jun 2025 21:35:31 GMT
ENV JAVA_SHA256=6600725ff08e343ea49db5bdac0cc8ef756053c899efb6a504b5f9e4a2fcc69d
# Tue, 10 Jun 2025 21:35:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:35:53 GMT
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
	-	`sha256:6affe3d610e676d5c4290e00d8682f9fbc342d58fa2aeb65aed764610ac714ea`  
		Last Modified: Tue, 10 Jun 2025 21:37:26 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5a1702dedccd0fff0ab31fc4e5db7c08a65dfcddb2119c0d9f06f3948c8668`  
		Last Modified: Tue, 10 Jun 2025 21:37:26 GMT  
		Size: 345.9 KB (345882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a70532f7eac9bb00ed6d5fb86f8a3bfeb72ec3b79ceb4b466a9ad89220182a7`  
		Last Modified: Tue, 10 Jun 2025 21:37:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f958a4743112bc9e0170430d7dd71bbaab05bfac2dd6b91460877a9d7428691`  
		Last Modified: Tue, 10 Jun 2025 21:37:26 GMT  
		Size: 334.5 KB (334514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7f961632a93b8244c92244783fcb899152e709bb64b4df1c560e8f7cf590fd`  
		Last Modified: Tue, 10 Jun 2025 21:37:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a5f6f1c6b319483940e51eb913762c0ed0e5db69e9328485d838f634b71365`  
		Last Modified: Tue, 10 Jun 2025 21:37:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a96e0b412469577904fe331b870c05ca906e92392b5ab9664c6feb899e8e509`  
		Last Modified: Tue, 10 Jun 2025 21:37:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb92a1b2b75c3ca9f233e8c8d18eced514dd85768f52a93bd82f97b8cf67ee9e`  
		Last Modified: Tue, 10 Jun 2025 22:09:34 GMT  
		Size: 218.8 MB (218802879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f15e011245b0d0a2106dba88fae619e4a844a327eaa0f7153bbb39c9f4060e4`  
		Last Modified: Tue, 10 Jun 2025 21:37:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<?xml version="1.0" encoding="UTF-8"?>

<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
	<xs:element name="AAAA-Message" type="T_AAAA-Message"/>
	<xs:element name="AAAA-Values" type="T_AAAA-Values"/>
	<xs:element name="Action" type="xs:string"/>
	<xs:element name="Advertiser" type="T_Advertiser"/>
	<xs:element name="AgeFrom" type="xs:byte"/>
	<xs:element name="AgeTo" type="xs:byte"/>
	<xs:element name="AvailLineWithDetailedPeriods" type="T_AvailLineWithDetailedPeriods"/>
	<xs:element name="AvailList" type="T_AvailList"/>
	<xs:element name="AvailName" type="xs:string"/>
	<xs:element name="BusinessObject" type="xs:string"/>
	<xs:element name="Buyer" type="T_Buyer"/>
	<xs:element name="BuyerName" type="xs:string"/>
	<xs:element name="Comment" type="T_Comment"/>
	<xs:element name="CommentLine" type="xs:string"/>
	<xs:element name="DayTime" type="T_DayTime"/>
	<xs:element name="DayTimes" type="T_DayTimes"/>
	<xs:element name="DaypartName" type="xs:string"/>
	<xs:element name="Days" type="T_Days"/>
	<xs:element name="DemoCategories" type="T_DemoCategories"/>
	<xs:element name="DemoCategory" type="T_DemoCategory"/>
	<xs:element name="DemoType" type="xs:string"/>
	<xs:element name="DemoValue" type="T_DemoValue"/>
	<xs:element name="DemoValues" type="T_DemoValues"/>
	<xs:element name="DetailedPeriod" type="T_DetailedPeriod"/>
	<xs:element name="Email" type="T_Email"/>
	<xs:element name="EndTime" type="xs:string"/>
	<xs:element name="Friday" type="xs:string"/>
	<xs:element name="Group" type="xs:string"/>
	<xs:element name="Media" type="xs:string"/>
	<xs:element name="Monday" type="xs:string"/>
	<xs:element name="Name" type="xs:string"/>
	<xs:element name="OutletReference" type="T_OutletReference"/>
	<xs:element name="OutletReferences" type="T_OutletReferences"/>
	<xs:element name="Outlets" type="T_Outlets"/>
	<xs:element name="Periods" type="T_Periods"/>
	<xs:element name="Phone" type="T_Phone"/>
	<xs:element name="Proposal" type="T_Proposal"/>
	<xs:element name="Rate" type="xs:short"/>
	<xs:element name="Salesperson" type="T_Salesperson"/>
	<xs:element name="Saturday" type="xs:string"/>
	<xs:element name="SchemaName" type="xs:string"/>
	<xs:element name="SchemaVersion" type="xs:string"/>
	<xs:element name="Seller" type="T_Seller"/>
	<xs:element name="SpotLength" type="xs:time"/>
	<xs:element name="SpotsPerWeek" type="xs:byte"/>
	<xs:element name="StartTime" type="xs:string"/>
	<xs:element name="Sunday" type="xs:string"/>
	<xs:element name="TargetDemo" type="T_TargetDemo"/>
	<xs:element name="TelevisionStation" type="T_TelevisionStation"/>
	<xs:element name="Thursday" type="xs:string"/>
	<xs:element name="Tuesday" type="xs:string"/>
	<xs:element name="UniqueMessageID" type="xs:string"/>
	<xs:element name="Wednesday" type="xs:string"/>
	<xs:attribute name="DemoId" type="xs:string"/>
	<xs:attribute name="buyingCompanyName" type="xs:string"/>
	<xs:attribute name="callLetters" type="xs:string"/>
	<xs:attribute name="companyName" type="xs:string"/>
	<xs:attribute name="demoRef" type="xs:string"/>
	<xs:attribute name="endDate" type="xs:date"/>
	<xs:attribute name="identifier" type="xs:string"/>
	<xs:attribute name="isPackage" type="xs:string"/>
	<xs:attribute name="name" type="xs:string"/>
	<xs:attribute name="outletForListId" type="xs:string"/>
	<xs:attribute name="outletFromListRef" type="xs:string"/>
	<xs:attribute name="outletFromProposalRef" type="xs:string"/>
	<xs:attribute name="outletId" type="xs:string"/>
	<xs:attribute name="parentPlus" type="xs:string"/>
	<xs:attribute name="sendDateTime" type="xs:dateTime"/>
	<xs:attribute name="startDate" type="xs:date"/>
	<xs:attribute name="type" type="xs:string"/>
	<xs:attribute name="uniqueIdentifier" type="xs:string"/>
	<xs:attribute name="version" type="xs:byte"/>
	<xs:attribute name="weekStartDay" type="xs:string"/>
	<xs:complexType name="T_AAAA-Message">
		<xs:sequence>
			<xs:element ref="AAAA-Values"/>
			<xs:element ref="Proposal"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_AAAA-Values">
		<xs:sequence>
			<xs:element ref="SchemaName"/>
			<xs:element ref="SchemaVersion"/>
			<xs:element ref="Media"/>
			<xs:element ref="BusinessObject"/>
			<xs:element ref="Action"/>
			<xs:element ref="UniqueMessageID"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_Advertiser">
		<xs:attribute ref="name" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_AvailLineWithDetailedPeriods">
		<xs:sequence>
			<xs:element ref="OutletReference"/>
			<xs:element ref="DayTimes"/>
			<xs:element ref="DaypartName"/>
			<xs:element ref="AvailName"/>
			<xs:element ref="SpotLength"/>
			<xs:element ref="Periods"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_AvailList">
		<xs:sequence>
			<xs:element ref="Name"/>
			<xs:element ref="OutletReferences"/>
			<xs:element ref="DemoCategories"/>
			<xs:element ref="TargetDemo"/>
			<xs:element ref="Comment"/>
			<xs:element ref="AvailLineWithDetailedPeriods" maxOccurs="unbounded"/>
		</xs:sequence>
		<xs:attribute ref="endDate" use="required"/>
		<xs:attribute ref="identifier" use="required"/>
		<xs:attribute ref="isPackage" use="required"/>
		<xs:attribute ref="startDate" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_Buyer">
		<xs:sequence>
			<xs:element ref="BuyerName"/>
		</xs:sequence>
		<xs:attribute ref="buyingCompanyName" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_Comment">
		<xs:sequence>
			<xs:element ref="CommentLine"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_DayTime">
		<xs:sequence>
			<xs:element ref="StartTime"/>
			<xs:element ref="EndTime"/>
			<xs:element ref="Days"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_DayTimes">
		<xs:sequence>
			<xs:element ref="DayTime"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_Days">
		<xs:sequence>
			<xs:element ref="Monday"/>
			<xs:element ref="Tuesday"/>
			<xs:element ref="Wednesday"/>
			<xs:element ref="Thursday"/>
			<xs:element ref="Friday"/>
			<xs:element ref="Saturday"/>
			<xs:element ref="Sunday"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_DemoCategories">
		<xs:sequence>
			<xs:element ref="DemoCategory"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_DemoCategory">
		<xs:sequence>
			<xs:element ref="DemoType"/>
			<xs:element ref="Group"/>
			<xs:element ref="AgeFrom"/>
			<xs:element ref="AgeTo"/>
		</xs:sequence>
		<xs:attribute ref="DemoId" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_DemoValue">
		<xs:simpleContent>
			<xs:extension base="xs:decimal">
				<xs:attribute ref="demoRef" use="required"/>
			</xs:extension>
		</xs:simpleContent>
	</xs:complexType>
	<xs:complexType name="T_DemoValues">
		<xs:sequence>
			<xs:element ref="DemoValue"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_DetailedPeriod">
		<xs:sequence>
			<xs:element ref="Rate"/>
			<xs:element ref="SpotsPerWeek" minOccurs="0"/>
			<xs:element ref="DemoValues"/>
		</xs:sequence>
		<xs:attribute ref="startDate" use="required"/>
		<xs:attribute ref="endDate" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_Email">
		<xs:simpleContent>
			<xs:extension base="xs:string">
				<xs:attribute ref="type" use="required"/>
			</xs:extension>
		</xs:simpleContent>
	</xs:complexType>
	<xs:complexType name="T_OutletReference">
		<xs:attribute ref="outletFromProposalRef"/>
		<xs:attribute ref="outletForListId"/>
		<xs:attribute ref="outletFromListRef"/>
	</xs:complexType>
	<xs:complexType name="T_OutletReferences">
		<xs:sequence>
			<xs:element ref="OutletReference"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_Outlets">
		<xs:sequence>
			<xs:element ref="TelevisionStation"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_Periods">
		<xs:sequence>
			<xs:element ref="DetailedPeriod"/>
		</xs:sequence>
	</xs:complexType>
	<xs:complexType name="T_Phone">
		<xs:simpleContent>
			<xs:extension base="xs:string">
				<xs:attribute ref="type" use="required"/>
			</xs:extension>
		</xs:simpleContent>
	</xs:complexType>
	<xs:complexType name="T_Proposal">
		<xs:sequence>
			<xs:element ref="Seller"/>
			<xs:element ref="Buyer"/>
			<xs:element ref="Advertiser"/>
			<xs:element ref="Name"/>
			<xs:element ref="Outlets"/>
			<xs:element ref="AvailList"/>
		</xs:sequence>
		<xs:attribute ref="endDate" use="required"/>
		<xs:attribute ref="sendDateTime" use="required"/>
		<xs:attribute ref="startDate" use="required"/>
		<xs:attribute ref="uniqueIdentifier" use="required"/>
		<xs:attribute ref="version" use="required"/>
		<xs:attribute ref="weekStartDay" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_Salesperson">
		<xs:sequence>
			<xs:element ref="Phone" maxOccurs="unbounded"/>
			<xs:element ref="Email"/>
		</xs:sequence>
		<xs:attribute ref="name" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_Seller">
		<xs:sequence>
			<xs:element ref="Salesperson"/>
		</xs:sequence>
		<xs:attribute ref="companyName" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_TargetDemo">
		<xs:attribute ref="demoRef" use="required"/>
	</xs:complexType>
	<xs:complexType name="T_TelevisionStation">
		<xs:attribute ref="callLetters" use="required"/>
		<xs:attribute ref="outletId" use="required"/>
		<xs:attribute ref="parentPlus" use="required"/>
	</xs:complexType>
</xs:schema>

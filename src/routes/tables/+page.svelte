<script>
	import * as Table from '$lib/components/ui/table/index';
	const invoices = [
		{
			invoice: 'INV001',
			paymentStatus: 'Paid',
			totalAmount: '$250.00',
			paymentMethod: 'Credit Card'
		},
		{
			invoice: 'INV002',
			paymentStatus: 'Pending',
			totalAmount: '$150.00',
			paymentMethod: 'PayPal'
		},
		{
			invoice: 'INV003',
			paymentStatus: 'Unpaid',
			totalAmount: '$350.00',
			paymentMethod: 'Bank Transfer'
		},
		{
			invoice: 'INV004',
			paymentStatus: 'Paid',
			totalAmount: '$450.00',
			paymentMethod: 'Credit Card'
		},
		{
			invoice: 'INV005',
			paymentStatus: 'Paid',
			totalAmount: '$550.00',
			paymentMethod: 'PayPal'
		},
		{
			invoice: 'INV006',
			paymentStatus: 'Pending',
			totalAmount: '$200.00',
			paymentMethod: 'Bank Transfer'
		},
		{
			invoice: 'INV007',
			paymentStatus: 'Unpaid',
			totalAmount: '$300.00',
			paymentMethod: 'Credit Card'
		}
	];
</script>

<main class="container">
	<div>Tables</div>

	<div class="flex w-full flex-col items-center justify-center border border-white">
		<Table.Root>
			<Table.Caption>All Invoices</Table.Caption>
		</Table.Root>
		<Table.Header>
			<Table.Row>
				<Table.Head class="w-[100px]">Invoice</Table.Head>
				<Table.Head>Status</Table.Head>
				<Table.Head>Method</Table.Head>
				<Table.Head class="text-right">Amount</Table.Head>
			</Table.Row>
			<Table.Body>
				{#each invoices as invoice, i (i)}
					<Table.Row>
						<Table.Cell>
							{invoice.invoice}
						</Table.Cell>
					</Table.Row>
				{/each}
			</Table.Body>
		</Table.Header>
	</div>
</main>

<style>
	.container {
		display: flex;
		flex-direction: column;
		height: 100%;
		margin: auto;
		justify-content: center;
		align-items: center;
		width: 60rem;
		margin-top: 2rem;
		background-color: black;
	}
</style>
